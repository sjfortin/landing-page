<template>
  <div id="app">
    <LandingPage msg="Sam Fortin" />
  </div>
</template>

<script>
import LandingPage from "./components/LandingPage.vue";

document.title = 'sjfortin';

export default {
  name: "app",
  components: {
    LandingPage
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
