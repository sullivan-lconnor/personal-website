<template>
    <div class="body">
      <div class="content">
        <h2>Blog Post 1</h2>
        <p>This is the content of the first blog post.</p>
        <!-- Add more blog posts here -->
      </div>
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .body {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    padding: 20px;
  }
  
  .content {
    width: 60%;
    background-color: white;
    color: black;
    padding: 20px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  
  @media (max-width: 1024px) {
    .content {
      width: 80%;
    }
  }
  
  @media (max-width: 600px) {
    .content {
      width: 100%;
      padding: 10px;
    }
  }
  </style>
  