<template>
    <div id="introduction">
        <section>
            <p> <Gif name="Hi" url="/static/gifs/hi-gif.webp"/> , I'm Theo or you can call me Tho - 🖖 </p>
            <p>A Web <Gif name="Developer" url="/static/gifs/developer-gif.webp"/> & Web Designer living in France.</p>
            <p>In my work my goal is to <Gif name="create" url="/static/gifs/create2-gif.webp"/> thoughtful, engaging and functional web applications that have a clean and distinct design.</p>
        </section>
    </div>
</template>

<script>
import Gif from './Gif.vue'

export default {
    name: 'Introduction',

    components: {
        Gif
    },
}
</script>

<style scoped lang="scss">
#introduction{
    font-size: 7vw;
    line-height: 140%;
    font-weight: 700;
    padding: 0 5rem 0 5rem;
}
</style>