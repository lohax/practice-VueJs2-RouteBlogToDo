<template>
  <div id="app">
    <header-top />
    <router-view></router-view>
    <!-- <header-top />
    <contenu /> -->
  </div>
</template>

<script>
import Header from "./components/Navigation.vue";

// import Header from "./components/Header.vue";
// import Contenu from "./components/Contenu.vue";
export default {
  name: "App",
  components: {
    "header-top": Header,
    // contenu : Contenu
  },
};
</script>

<style>
</style>
