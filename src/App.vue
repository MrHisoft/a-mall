<template>
  <div id="app">
    <div id="nav">
      <Home />
      <router-view />
    </div>
  </div>
</template>
<script>
import Home from "./views/Home";
export default {
  components:{
    Home
  }
};
</script>
<style>
@import "assets/css/base.css";
</style>
