<template>
    <main>
        <section class="introduction">
            <p> <Gif name="Hi" url="/static/gifs/hi-gif.webp"/> , I'm Theo or you can call me Tho - 🖖 </p>
            <p>A Front-end <Gif name="Developer" url="/static/gifs/developer2-gif.webp"/> & UI/UX designer living in France.</p>
            <p>In my work my goal is to <Gif name="create" url="/static/gifs/create-gif.webp"/> thoughtful, engaging and functional web applications that have a clean and distinct design.</p>
        </section>
    </main>
</template>

<script>
import Gif from './features/Gif.vue'

export default {
    name: 'MainContent',

    components: {
        Gif
    },

    methods: {
        skewEffect(){
            const section = document.querySelector('section');
            let currentPos = window.pageYOffset;
            const skewAmount = 0.4;

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

<style scoped lang="scss">
main{
    font-size: 6.875rem;
    line-height: 8rem;
    font-weight: 700;
    padding: 0 5rem 0 5rem;

    section{
        transition: transform .1s;
    }
}
</style>