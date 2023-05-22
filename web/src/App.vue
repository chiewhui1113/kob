<template>
  <NavBar />
  <router-view/>
</template>

<script>
import NavBar from './components/NavBar.vue'
import "bootstrap/dist/css/bootstrap.min.css"
import "bootstrap/dist/js/bootstrap"

export default {
  components: {
    NavBar
  }, 
  setup() {

  }
}
</script>

<style>
body {
  background-image: url("./assets/images/aespa_bg.jpg");
  background-size: cover;
}
</style>
