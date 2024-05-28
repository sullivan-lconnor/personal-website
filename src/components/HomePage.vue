<template>
  <div class="home-page">
    <TopBanner />
    <Body />
  </div>
</template>

<script setup>
import TopBanner from './TopBanner.vue';
import Body from './Body.vue';
</script>

<style scoped>
.home-page {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 100%;
  background-color: #f0f0f0;
  flex: 1;
}
</style>
