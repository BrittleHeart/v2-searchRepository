<template>
  <h1> {{ name }} </h1>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'App',
  setup() {
    const name = ref('Bartosz')

    return { name }
  }
}
</script>

<style>
#app {
  font-family: 'Mont';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
