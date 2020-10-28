<template>
  <div id="app">
    <Navbar/>
    <router-view/>
  </div>
</template>

<script>
import Navbar from './components/Navbar'

export default {
  components: {
    Navbar,
  },

  mounted(){
    //Animation on view
    this.transitionOnView('work-description','fade-from-left');
    this.transitionOnView('work-title','fade-from-right');
    this.transitionOnView('skills-item','fade-from-left')
  },

  methods:{

    //Target must be a Class 
    transitionOnView(target, animationName){
      var elements;
      var windowHeight;

      function init() {
        elements = document.getElementsByClassName(target);
        windowHeight = window.innerHeight;
      }

      function checkPosition() {

        elements.forEach(element => {

          var positionFromTop = element.getBoundingClientRect().top;

          if (positionFromTop - windowHeight < 0) {
            element.classList.add(animationName);
            element.classList.remove('animate');
          }
          else if (positionFromTop - windowHeight > 0) {
            element.classList.remove(animationName);
            element.classList.add('animate');
          }
        });
      }

      window.addEventListener('scroll', checkPosition);
      window.addEventListener('resize', init);

      init();
      checkPosition();
    }

  }
}
</script>

<style lang="scss">
html{
  scroll-behavior: smooth;
}

*{
  box-sizing: border-box;
}

#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  color: #000000;
  margin: 0;
  box-sizing: border-box;
  padding: 0% 15% 0% 15%;
}

body {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

a {
  text-decoration: none;
  color: inherit;
}

li { 
  list-style: none;
  text-decoration: none;
}

//ANIMATIONS

.animate{
  transition: opacity 0.3s;
  opacity: 0;
}

//Fade from Right
@keyframes fade-right {
    from {opacity: 0; transform: translate(25rem);}
    to {opacity: 1; transform: translate(0);}
}

.fade-from-right{
  animation: fade-right 1s;
}

//Fade from left
@keyframes fade-left {
    from {opacity: 0; transform: translate(-25rem);}
    to {opacity: 1; transform: translate(0);}
}

.fade-from-left{
  animation: fade-left 1s ease;
}

//Fade from Right
@keyframes fade-bottom {
    from {opacity: 0; transform: translateY(25rem);}
    to {opacity: 1; transform: translateY(0);}
}

.fade-from-bottom{
  animation: fade-bottom 1s;
}


//SCROLLBAR
::-webkit-scrollbar-track {
	-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.1);
	background-color: #F5F5F5;
	border-radius: 10px;
}

::-webkit-scrollbar {
	width: 10px;
	background-color: #F5F5F5;
}

::-webkit-scrollbar-thumb {
	border-radius: 10px;
	background-color: #FFF;
	background-image: 
  -webkit-gradient(linear,40% 0%, 75% 84%, from(#83d2ff), to(#0645AD), color-stop(.6,#8a68e6))
}
</style>