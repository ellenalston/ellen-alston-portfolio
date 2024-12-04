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
}
</style>
