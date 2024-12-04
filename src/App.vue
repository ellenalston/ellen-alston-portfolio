<script setup>
import BannerContent from '@/components/BannerContent.vue'
import { RouterView } from 'vue-router'
</script>

<template>
  <BannerContent />
  <RouterView />
</template>

<style global>
body {
  font-family: "Karla", sans-serif !important;
  margin: 0;
  padding: 0;
}

html, body {
  height: 100%; /* Ensures the content height covers the viewport */
}

#app {
  min-height: 100%; /* Ensures the app container respects full height */
  display: flex;
  flex-direction: column;
}

router-view {
  flex: 1; /* Ensures content takes up available space */
  margin-top: 15vh; /* Adjust based on the banner height */
  z-index: 1; /* Lower than the banner's z-index */
}
</style>

