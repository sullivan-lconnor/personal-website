<template>
  <div class="top-banner">
    <div class="title">
      <label class="title1">Wow! A functioning webpage!?</label>
      <label class="title2">&nbsp;&nbsp;&nbsp;&nbsp;- Liam Sullivan</label>
    </div>
    <div class="icon-links">
      <BubbleLink iconSrc="src/assets/gihub_bubble.jpg" linkUrl="https://github.com/sullivan-lconnor" />
      <BubbleLink iconSrc="src/assets/linkedin_bubble.jpg" linkUrl="https://www.linkedin.com/in/liam-sullivan-22286415a/" />
    </div>
  </div>
</template>

<script setup>
import BubbleLink from './BubbleLink.vue';
</script>

<style scoped>
.top-banner {
  width: 100%;
  height: 120px;
  display: flex;
  align-items: center;
  justify-content: left;
  color: white;
  text-align: left;
  position: relative;
  overflow: hidden;
  background: url('src/assets/mosic.webp') repeat-x;
  animation: panBackground 200s linear infinite;
}

.title {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  background-color: rgba(69, 51, 71, 0.867); 
  color: rgb(223, 240, 253);
  height: 100px;
  padding: 0 20px;
  border-top-right-radius: 10px; /* Round top-right corner */
  border-bottom-right-radius: 10px; /* Round bottom-right corner */
  text-align: left;
}

.title1, .title2 {
  font-family: Arial, sans-serif;
  color: white;
  text-transform: uppercase;
  font-weight: bold; /* Make the text bold */
}

.title1 {
  font-size: 2.1em;
}

.title2 {
  font-size: 1.9em;
}

@keyframes panBackground {
  0% {
    background-position: 0 0;
  }
  100% {
    background-position: -1980px 0;
  }
}

.icon-links {
  position: absolute;
  right: 20px;
  display: flex;
  align-items: center;
}

@media (max-width: 600px) {
  .top-banner {
    height: 50px;
    font-size: 14px;
  }
  .icon-links {
    right: 10px;
  }
}
</style>