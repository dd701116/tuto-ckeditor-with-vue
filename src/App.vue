<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <ckeditor :editor="editor" v-model="editorData" :config="editorConfig"></ckeditor>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ClassicEditor from '@ckeditor/ckeditor5-build-classic';
export default {
  name: 'App',
  components: {
    HelloWorld
  },
        data() {
            return {
                editor: ClassicEditor,
                editorData: '<p>Content of the editor.</p>',
                editorConfig: {
                    // The configuration of the editor.
                }
            };
        }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
