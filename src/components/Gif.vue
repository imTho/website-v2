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
                        gif.style.top = `calc(${e.pageY}px - 300px)`; 
                        gif.style.left = `calc(${e.pageX}px - 150px)`;
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
            opacity: .95;
            pointer-events: none;
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