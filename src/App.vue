<script setup> // Vue 3's Composition API
import BannerContent from '@/components/BannerContent.vue' // import the BannerContent component
import { RouterView } from 'vue-router' // import the RouterView component, built-in with Vue Router
</script>

<template>
  <BannerContent /> <!--Render the BannerContent component-->
  <RouterView /> <!--Render the RouterView component-->
</template>

<style scoped>
body {
  font-family: "Karla", sans-serif !important; /* imporant to override the global font-family */
  margin: 0;
  padding: 0;
}

html, body {
  height: 100%; /* Ensures the content height covers the viewport */
}

#app { /* The app container */
  min-height: 100%; /* Ensures the app container respects full height */
  display: flex; /* Use flexbox for layout */
  flex-direction: column; /* Stack elements vertically */
}

router-view {
  flex: 1; /* Ensures content takes up available space */
  margin-top: 15vh; /* Adjust based on the banner height */
  z-index: 1; /* Lower than the banner's z-index */
}
</style>

