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
*, *::before, *::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  min-width: 100vw;
}

html, body {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

#app {
  width: 100%;
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
