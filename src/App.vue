<template>
  <div>
    <NavbarBase/>
    <!--
      <img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Welcome to Your Vue.js App" />
    -->
    
    <TopParallax/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import NavbarBase from './components/structure/NavbarBase.vue'
import TopParallax from './components/parallax/TopParallax.vue'
//import BoostrapTest from './components/BoostrapTest.vue'
//import ImageCarousel from './components/Images/ImageCarousel.vue'

export default {
  name: 'App',
  components: {
    NavbarBase,
    TopParallax,

  }
}
</script>

<style>
</style>
