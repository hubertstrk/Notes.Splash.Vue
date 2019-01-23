<template>
  <div id="app">
    <hello-world />
  </div>
</template>

<script>
import 'spectre.css/dist/spectre.min.css'
import 'spectre.css/dist/spectre-exp.min.css'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
</script>

<style lang="css">
body {
  height: 300px;
  width: 600px;
  margin: 0;
  padding: 0;
}
</style>
