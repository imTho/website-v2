<template>
    <div id="introduction">
        <section>
            <p> <Gif name="Hi" url="/static/gifs/hi-gif.webp"/> , I'm Theo or you can call me Tho - 👋 </p>
            <p>A Front-end <Gif name="Developer" url="/static/gifs/developer-gif.webp"/> living in France.</p>
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
    font-size: 6vw;
    line-height: 140%;
    font-weight: 700;
    margin-top: 12rem;
    cursor: default;
}

@media (max-width: 775px) {
    #introduction{
        font-size: 11vw;
    }
}
</style>