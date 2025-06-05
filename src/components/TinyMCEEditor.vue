<template>
  <textarea id="editor"></textarea>
</template>

<script setup lang="ts">
import { onMounted, onBeforeUnmount } from 'vue';

onMounted(() => {
  tinymce.init({
    selector: '#editor',
    apiKey: 'ajzwlify6vbdufx0b0egj9mbea4cq1sh2ds59xzrde9mryly',
    plugins: 'mathType chemType',
    toolbar: 'undo redo | bold italic | mathType chemType',
    readonly: false,
  });
});

onBeforeUnmount(() => {
  tinymce.remove('#editor');
});
</script>
