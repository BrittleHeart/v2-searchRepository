<template>
  <search-wrapper>
    <search-toolbar />
  </search-wrapper>
</template>

<script>
import searchWrapper from '@/components/searchWrapper'
import searchToolbar from '@/components/searchToolbar'

export default {
  name: 'App',
  components: {
    searchWrapper,
    searchToolbar, 
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
  background: #E0E0E0 none;
}

html, body {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

#app {
  width: 60%;
  margin: 0 auto;
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
