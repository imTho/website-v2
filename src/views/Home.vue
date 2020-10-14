<template>
  <div class="home">
    <Navbar/>
    <Introduction/>
    <Work/>
  </div>
</template>

<script>
import Introduction from '../components/Introduction';
import Navbar from '../components/Navbar';
import Work from '../components/Work';

export default {
  name: 'Home',

  components: {
    Introduction,
    Navbar,
    Work
  },

  methods: {
        skewEffect(){
            const section = document.querySelector('section');
            let currentPos = window.pageYOffset;
            const skewAmount = 0.3;

            const looper = function() {
                const newPos = window.pageYOffset;
                const diff = newPos - currentPos;
                const speed = diff * skewAmount;
                
                section.style.transform = `skewY(${speed}deg)`;
                currentPos = newPos;
                
                requestAnimationFrame(looper);
            }
            looper();   
        }
    },

    mounted(){
        this.skewEffect()
    },
}
</script>

<style lang="scss">
  section{
        transition: transform .1s;
    }
</style>