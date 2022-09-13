<script>
import HomePage from "./pages/HomePage.vue";
import BaseHeader from "./components/BaseHeader.vue";
import BaseFooter from "./components/BaseFooter.vue";

export default {
  components: {
    HomePage,
    BaseHeader,
    BaseFooter
  }
}
</script>

<template>
  <div class="app">
    <base-header />
    <home-page />
    <base-footer />
  </div>
</template>

<style>
body {
  margin: 0;
}

</style>
