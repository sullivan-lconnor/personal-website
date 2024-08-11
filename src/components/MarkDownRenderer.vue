<template>
    <div v-html="renderedMarkdown"></div>
  </template>
  
  <script>
  import MarkdownIt from 'markdown-it';
  
  export default {
    name: 'MarkdownRenderer',
    props: {
      content: {
        type: String,
        required: true,
      },
    },
    data() {
      return {
        markdown: new MarkdownIt(),
      };
    },
    computed: {
      renderedMarkdown() {
        // Render the markdown content to HTML
        return this.markdown.render(this.content);
      },
    },
  };
  </script>
  
  <style scoped>
  div {
    font-family: Arial, sans-serif;
  }
  </style>
  