<template>
  <div class="body">
    <div class="content">
      <MarkdownEditor />
      <MarkdownPost mdPath="src/assets/blog_posts/Post2_reverse_proxies.md" />
      <MarkdownPost mdPath="src/assets/blog_posts/Post1_how_it_all_works.md" />
    </div>
  </div>
</template>

<script setup>
import MarkdownPost from './MarkDownPost.vue';
import MarkdownEditor from './MarkDownEditor.vue';
</script>

<style scoped>
.body {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  padding: 20px;
  width: 100%;
  overflow-y: auto;
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
