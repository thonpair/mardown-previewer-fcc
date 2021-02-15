<template>
  <div id="app">
    <textarea id="editor" v-model="markdownText">  
  </textarea>
    <div id="preview">
      <VueMarkdown :source="markdownText"></VueMarkdown>
  </div>

  </div>
</template>

<script>
import VueMarkdown from 'vue-markdown'
export default {
  name: 'App',
  components: {
    VueMarkdown
  },
  data(){
    return {
      markdownText :  String,
    }
  },
  created(){
    this.markdownText = "a\n# h1 Heading\n## h2 Heading\n[link text](https://emmanuel.hemer.it)\nInline `code`\n```\nSample text here...\n```\n+ list item 1\n+ list item 2\n> Blockquote\n![Stormtroopocat](https://octodex.github.com/images/stormtroopocat.jpg \"The Stormtroopocat\")\n**This is bold text**"
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
#editor{
  width: 500px;
  height:300px;
}
</style>
