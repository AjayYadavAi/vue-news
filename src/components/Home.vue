<template>
	<div class="home">
    <div class="content-wrapper">
      <div class="container">
        <div class="col-sm-12">
          <div class="card">
            <div class="card-body">
              <div class="row">
                <div class="col-sm-12">
                  <h1 class="font-weight-600 mb-4">
                    Today News 
                  </h1>
                </div>
              </div>
              <div class="row">
                <div class="col-lg-12" v-for="(news,i) in newslist" :key="i">
                  <div class="row">
                    <div class="col-sm-4 grid-margin">
                      <div class="rotate-img">
                        <img
                          :src="news.urlToImage"
                          alt="banner"
                          class="img-fluid"
                        />
                      </div>
                    </div>
                    <div class="col-sm-8 grid-margin">
                      <h2 class="font-weight-600 mb-2">
                        {{ news.title }}
                      </h2>
                      <p class="fs-13 text-muted mb-0">
                        <span class="mr-2">Photo </span>{{ news.publishedAt }}
                      </p>
                      <p class="fs-15">
                        {{ news.description }}
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div> 
  </div>
</template>

<script>
export default {
	name: 'home',
	data(){
		return {
			url:process.env.BASE_URL,
      newslist:[],
		}
	},
  mounted(){
    this.latesNews();
  },
  methods:{
    async latesNews(){
      var api = "https://newsapi.org/v2/top-headlines?country=in&apiKey="+process.env.VUE_APP_API_KEY;
      const res = await fetch(api);
      const data = await res.json();
      this.newslist = data.articles;
      console.log(this.newslist);
    },
  }
}
</script>