<template>
    <div class="editor-container">
      <div class="editor-header">
        <button @click="submitMarkdown">Submit</button>
      </div>
      <div class="editor-body">
        <textarea v-model="markdownText" class="editor-textarea"></textarea>
        <div class="editor-preview">
          <MarkdownRenderer :content="markdownText" />
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import MarkdownRenderer from './MarkDownRenderer.vue';
  
  const markdownText = ref('');
  
  function submitMarkdown() {
    // Placeholder function for submit button
    console.log("Submit button clicked");
  }
  </script>
  
  <style scoped>
  .editor-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  .editor-header {
    width: 100%;
    display: flex;
    justify-content: flex-end;
    margin-bottom: 10px;
  }
  
  .editor-body {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
  
  .editor-textarea {
    width: 48%;
    height: 400px;
    padding: 10px;
    font-family: monospace;
    font-size: 16px;
    border: 1px solid #ccc;
    resize: none;
  }
  
  .editor-preview {
    width: 48%;
    height: 400px;
    padding: 10px;
    border: 1px solid #ccc;
    overflow-y: auto;
  }
  </style>
  
