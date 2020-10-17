<template>
    <span class="highlighted" @mouseover="showGif()" @mouseleave="visible = false">  {{name}}
        <transition name="fade">
            <img v-show="visible" :class="name" :src="url" alt="">
        </transition>
    </span>
</template>

<script>
    export default {
        name: 'Gif',

        props: {
            name: {
                type: String,
                required: true,
            },
            url: {
                type: String,
            }
        },

        data() {
            return {
                visible: false,
            };
        },

        mounted(){

        },

        methods: {
            showGif(){
                this.visible = true;
                let gif = this.$el.children[0];

                console.log(gif);
                document.onmousemove = function(e){
                    setTimeout(function() {
                        gif.style.top = `calc(${e.pageY}px - 12rem)`; 
                        gif.style.left = `calc(${e.pageX}px - 9%)`;
                    },150) 
                } 
            }
        },
    }
</script>

<style scoped lang="scss">
.highlighted{
    cursor: pointer;
    color: #0645AD;
    text-decoration: underline;

        img{
            width: 40vw;
            position: absolute;
            // top: calc(0px - 12rem);
            // left: calc(0px - 8%);
            opacity: .95;
            pointer-events: none;
            z-index: 100;
        }
}

@media (max-width: 775px) {
    .highlighted{
        img{
            width: 80vw !important;
        }
    }
}

// Animation transition
.fade-enter-active, .fade-leave-active {
    transition: opacity .5s !important;
}

.fade-enter, .fade-leave-to {
    opacity: 0 !important;
}
</style>