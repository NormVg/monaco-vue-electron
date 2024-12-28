<script setup>

import { VueMonacoEditor } from '@guolao/vue-monaco-editor';

import { ref, shallowRef } from 'vue'

const MONACO_EDITOR_OPTIONS = {
  automaticLayout: true,
  formatOnType: true,
  formatOnPaste: true,
}

const code = ref('// some code...')
const editorRef = shallowRef()
const handleMount = editor => (editorRef.value = editor)


</script>


<template>
  <VueMonacoEditor
  v-model:value="code"
    theme="vs-dark"
    :options="MONACO_EDITOR_OPTIONS"
    @mount="handleMount"
    height="96vh"
    language="javascript"
  />
</template>
