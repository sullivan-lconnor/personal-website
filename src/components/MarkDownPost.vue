<template>
  <MarkdownRenderer :content="content" class="markdown-post" />
</template>

<script setup>
import { ref, onMounted } from 'vue';
import MarkdownRenderer from './MarkDownRenderer.vue';

const props = defineProps({
  mdPath: {
    type: String,
    required: true,
  },
});

const content = ref('');

onMounted(async () => {
  const response = await fetch(props.mdPath);
  content.value = await response.text();
});
</script>

<style scoped>
.markdown-post {
  padding: 20px;
  margin: 10px;
  background-color: white;
  color: black;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  text-align: left;
}
</style>
