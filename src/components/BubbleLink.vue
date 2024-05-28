<template>
  <a :href="linkUrl" target="_blank" class="bubble-link">
    <img :src="iconSrc" alt="link icon" class="icon">
  </a>
</template>

<script setup>
defineProps({
  iconSrc: {
    type: String,
    required: true
  },
  linkUrl: {
    type: String,
    required: true
  }
});
</script>

<style scoped>
.bubble-link {
  display: inline-block;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  overflow: hidden;
  background-color: rgba(69, 51, 71, 0.867); 
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  margin: 0 10px;
  transition: transform 0.3s ease;
}

.bubble-link:hover {
  transform: scale(1.1);
}

.icon {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
