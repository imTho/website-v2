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
}


</script>

<style scoped lang="scss">
main{
    font-size: 6.875rem;
    line-height: 8rem;
    font-weight: 700;
    padding: 0 5rem 0 5rem;
}
</style>