<template>
	<header id="header">
		<div class="container">
			<header id="header">
				<div class="container">
					<nav class="navbar navbar-expand-lg navbar-light">
		                <div class="navbar-bottom">
		                	<div class="d-flex justify-content-between align-items-center">
		                  		<div>
		                    		<a class="navbar-brand" href="#">
		                    			<img :src="`${url}theme/assets/images/logo.svg`" alt=""/>
		                    		</a>
		                    	</div>
		                    <div>
		                    <button
		                      class="navbar-toggler"
		                      type="button"
		                      data-target="#navbarSupportedContent"
		                      aria-controls="navbarSupportedContent"
		                      aria-expanded="false"
		                      aria-label="Toggle navigation"
		                    >
		                      	<span class="navbar-toggler-icon"></span>
		                    </button>
		                    <div
		                      class="navbar-collapse justify-content-center collapse"
		                      id="navbarSupportedContent"
		                    >
		                      <ul
		                        class="navbar-nav d-lg-flex justify-content-between align-items-center"
		                      >
		                        <li>
		                          <button class="navbar-close">
		                            <i class="mdi mdi-close"></i>
		                          </button>
		                        </li>
		                        <li class="nav-item active">
		                          <a class="nav-link" href="../index.html">Home</a>
		                        </li>
		                      </ul>
		                    </div>
		                  </div>
		                  <ul class="social-media">
		                    <li>
		                      <a href="#">
		                        <i class="mdi mdi-facebook"></i>
		                      </a>
		                    </li>
		                    <li>
		                      <a href="#">
		                        <i class="mdi mdi-youtube"></i>
		                      </a>
		                    </li>
		                    <li>
		                      <a href="#">
		                        <i class="mdi mdi-twitter"></i>
		                      </a>
		                    </li>
		                  </ul>
		                </div>
		              </div>
		            </nav>
	          </div>
        	</header>
        </div>
     </header>
</template>

<script>
export default {
  name: 'header',
  data(){
  	return {
  		url: process.env.BASE_URL
  	}
  }
}
</script>