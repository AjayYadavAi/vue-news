<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <header></header>
    
    <footer></footer>
  </div>
</template>

<script>
import Header from './components/Header'
import Footer from './components/Footer'
export default {
  name: 'App',
  components: {
    'header': Header,
    'footer': Footer
  }
}
</script>
