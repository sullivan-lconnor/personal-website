<template>
    <div v-html="content" class="blog-post"></div>
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue';
  import { marked } from 'marked';
  
  const props = defineProps({
    mdPath: {
      type: String,
      required: true
    }
  });
  
  const content = ref('');
  
  onMounted(async () => {
    const response = await fetch(props.mdPath);
    const markdown = await response.text();
    content.value = marked(markdown);
  });
  </script>
  
  <style scoped>
  .blog-post {
    padding: 20px;
    margin: 10px;
    background-color: white;
    color: black;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    text-align: left; /* Add this line to left-align the text */
  }
  </style>
  