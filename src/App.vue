<script>
import HomePage from "./pages/HomePage.vue";
import BaseLayout from "./components/BaseLayout.vue";

export default {
  components: {
    HomePage,
    BaseLayout
  }
}
</script>

<template>
  <BaseLayout>
    <HomePage />
  </BaseLayout>
</template>

<style>
body {
  margin: 0;
}

</style>
