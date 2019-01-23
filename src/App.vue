<template>
  <div id="app">
    <hello-world />
  </div>
</template>

<script>
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
  height: 400px;
  width: 400px;
  margin: 0;
  padding: 0;
}
</style>
