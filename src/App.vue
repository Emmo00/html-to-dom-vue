<script setup>
import { ref } from 'vue';

const html = ref("<h1>Hello world</h1>\n\n<p>This is a paragraph translated from html to DOM in vue</p>");
</script>

<template>
  <div style="height: 90vh;">
    <header>HTML to DOM</header>
    <div class="editor-container">
      <div class="editor-input-container"><textarea name="html" id="html" cols="30" rows="10" v-model="html"
          class="editor-input"></textarea></div>
      <div class="editor-preview-container">
        <div v-html="html" class="editor-preview"></div>
      </div>
    </div>
  </div>
</template>

<style scoped>
header {
  height: 60px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: xx-large;
}

.editor-container {
  display: flex;
  justify-content: center;
  height: 100%;
  gap: 5px
}

.editor-input-container {
  height: 100%;
  width: 50%;

  textarea {
    border-radius: 7px;
    width: 100%;
    height: 90%;
    border: 20px dotted grey;
  }
}

@media screen and (max-width: 599px) {
  .editor-container {
    flex-direction: column;
    justify-content: flex-start;
    padding: 5px;
  }

  .editor-input-container {
    height: 50%;
    width: 100%
  }
}
</style>