<template>
  <div id="app">
    <router-view></router-view>
    <main-tab-bar></main-tab-bar>
  </div>
</template>

<script>
  import mainTabBar from './components/content/mainTabBar'
export default {
  name: 'App',
  components: {
    mainTabBar,
  },
  data(){
    return{
      isActive:false
    }
  }
}
</script>

<style>
@import "assets/css/base.css";

</style>
