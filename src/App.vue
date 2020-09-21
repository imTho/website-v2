<template>
  <div id="app">
    <Navbar/>
    <MainContent/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import MainContent from './components/MainContent.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    MainContent
  }
}
</script>

<style lang="scss">
body{
  margin: 0;
  padding: 0;
  overflow-x: hidden;
  box-sizing: border-box;
}

#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #000000;
  margin: 0;
  padding-left: 14rem;
}

li{
  list-style: none;
  text-decoration: none;
}

a{
  text-decoration: none;
  color: inherit;
}
</style>
