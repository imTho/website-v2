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

        methods: {
            showGif(){
                this.visible = true;
                let gif = this.$el.children[0];
                window.onmousemove = function(e){
                    setTimeout(function() {
                        gif.style.top =  'calc(' + e.pageY + 'px - 10%)'; 
                        gif.style.left = 'calc(' + e.pageX + 'px - 10%)';
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
                opacity: .95;
                position: absolute;
                pointer-events: none;
            }
    }

    // Animation transition
    .fade-enter-active, .fade-leave-active {
        transition: opacity .20s !important;
    }

    .fade-enter, .fade-leave-to {
        opacity: 0 !important;
    }
</style>