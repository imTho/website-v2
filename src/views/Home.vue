<template>
  <div class="home">
    <Navbar/>
    <Introduction/>
    <Work/>
    <Skills/>
    <Footer/>
  </div>
</template>

<script>
import Introduction from '../components/Introduction';
import Navbar from '../components/Navbar';
import Work from '../components/Work';
import Skills from '../components/Skills';
import Footer from '../components/Footer';

export default {
  name: 'Home',

  components: {
    Introduction,
    Navbar,
    Work,
    Skills,
    Footer
  },

  methods: {
        skewEffect(){
            const sections = document.querySelectorAll('section');
            let currentPos = window.pageYOffset;
            const skewAmount = 0.3;

            const looper = function() {
                const newPos = window.pageYOffset;
                const diff = newPos - currentPos;
                const speed = diff * skewAmount;
                const maxSpeed = 12;
                
                sections.forEach(section => {
                  if(speed < maxSpeed){
                    section.style.transform = `skewY(${speed}deg)`;
                    currentPos = newPos;
                  }
                  else{
                    section.style.transform = `skewY(${maxSpeed}deg)`;
                    currentPos = newPos;
                  }
                });
                
                requestAnimationFrame(looper);
            }
            looper();   
        }
    },

    mounted(){
      if(window.innerWidth > 775){
        this.skewEffect()
      }  
    },
}
</script>

<style lang="scss">
  section{
        transition: transform .1s;
    }
</style>