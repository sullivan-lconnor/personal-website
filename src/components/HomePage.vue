<template>
  <div class="home-page" :style="{ backgroundImage: `url(${mosaicBackground})` }">
    <TopBanner />
    <Body />
  </div>
</template>

<script setup>
import TopBanner from './TopBanner.vue';
import Body from './Body.vue';
import mosaicBackground from '@/assets/background_mosaic.jpg'; // Corrected path using @ alias
</script>

<style scoped>
.home-page {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 100%;
  background-size: cover; /* Ensure the background covers the entire area */
  background-repeat: no-repeat; /* Prevent background repetition */
  background-attachment: fixed; /* Keep the background fixed on scroll */
}
</style>
