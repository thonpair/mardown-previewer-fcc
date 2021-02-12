<template>
  <div id="app">
    <textarea id="editor" v-model="markdownText">  
  </textarea>
    <Preview :markdownText="markdownText" />
  </div>
</template>

<script>
import Preview from './components/Preview'

export default {
  name: 'App',
  components: {
    Preview
  },
  data(){
    return {
      markdownText : "tot"
    }
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
