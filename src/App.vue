<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div class="container">
    <page-home></page-home>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import PageHome from "./components/PageHome.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    PageHome,
  },
};
</script>

<style>
@import "assets/style.css";
</style>
