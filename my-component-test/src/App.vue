<template>
  <div id="app">
    <img src="./assets/logo.png"
    @click="goBackHomePage">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods:{
    goBackHomePage(){
      this.$router.push({path:'/'})
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: right;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
