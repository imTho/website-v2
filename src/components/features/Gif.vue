<template>
    <span class="highlighted" @mouseenter="showGif()" @mouseleave="visible = false">  {{name}}
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

        methods: {
            showGif(){
                this.visible = true;
                let gifName = this.name;
                let gifs = document.querySelectorAll('.highlighted');

                gifs.forEach(gif => {
                    if(gif.children[0].classList.contains(gifName) && this.visible == true){
                        window.onmousemove = function(e){
                            gif.children[0].style.top = e.pageY + "px";
                            gif.children[0].style.left = e.pageX + "px";
                        }
                    }
                })
            }
        }
    }
</script>

<style scoped lang="scss">
    .highlighted{
        cursor: pointer;
        color: #0645AD;
        text-decoration: underline;

            img{
                position: absolute;
                pointer-events:none;
            }
    }

    // Animation transition
    .fade-enter-active, .fade-leave-active {
        transition: opacity .20s;
    }

    .fade-enter-to, .fade-leave {
        opacity: 0.95;
    }

    .fade-enter, .fade-leave-to {
        opacity: 0;
    }
</style>