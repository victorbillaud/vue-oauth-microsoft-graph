<script>
import BaseHeader from "./BaseHeader.vue";
import BaseFooter from "./BaseFooter.vue";

export default {
    components: {
        BaseHeader,
        BaseFooter
    }
}
</script>

<template>
    <div class="app">
      <base-header />
      <slot />
      <base-footer />
    </div>
</template>