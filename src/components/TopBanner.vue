<template>
    <div class="top-banner">
      <h1>Welcome to My Personal Website</h1>
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .top-banner {
    width: 100%;
    height: 60px;
    background-color: #4CAF50;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    text-align: center;
  }
  
  @media (max-width: 600px) {
    .top-banner {
      height: 50px;
      font-size: 14px;
    }
  }
  </style>
  