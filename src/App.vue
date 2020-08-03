<template>
  <div id="app">
    <Kickstarter/>
    <Navigation />
    <BannerImage/>
    <router-view></router-view>
  </div>
</template>

<script>
import Kickstarter from './components/Kickstarter.vue'
import Navigation from './components/Navigation.vue'
import BannerImage from './components/BannerImage.vue'
/*import PromoCode from './components/PromoCode.vue'*/

export default {
  name: 'App',
  components: {
    Kickstarter,
    Navigation,
    BannerImage
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width:100%;

}
body{
  margin: 0px;

}
</style>
