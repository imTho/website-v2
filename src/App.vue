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

//ScrollBar
::-webkit-scrollbar-track
{
	-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.1);
	background-color: #F5F5F5;
	border-radius: 10px;
}

::-webkit-scrollbar
{
	width: 10px;
	background-color: #F5F5F5;
}

::-webkit-scrollbar-thumb
{
	border-radius: 10px;
	background-color: #FFF;
	background-image: 
  -webkit-gradient(linear,40% 0%, 75% 84%, from(#83d2ff), to(#0645AD), color-stop(.6,#8a68e6))
}
</style>
