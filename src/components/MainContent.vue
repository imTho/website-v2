<template>
    <main>
        <section class="introduction">
            <p> <Gif name="Hi" url="/static/gifs/hi-gif.webp"/> , I'm Theo or you can call me Tho - 🖖 </p>
            <p>A Front-end <Gif name="Developer" url="/static/gifs/developer-gif.webp"/> & UI/UX designer living in France.</p>
            <p>In my work my goal is to <Gif name="create" url=""/> thoughtful, engaging and functional web applications that have a distinct and clean design.</p>
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
    font-size: 110px;
    line-height: 130px;
    font-weight: 700;
    margin-left: 105px;
    padding-left: 180px;
}
</style>