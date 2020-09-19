<template>
    <span class="highlighted" @mouseenter="showGif()" @mouseleave="enable = false">  {{name}}
        <img v-show="enable" :class="name" :src="url" alt="">
    </span>
</template>

<script>
    export default {
        name: 'Gif',

        props: [
            'name',
            'url'
        ],

        data:function() {
            return {
                enable: false,
            };
        },

        methods: {
            showGif(){
                this.enable = true;
                window.onmousemove = function(e){
                    let gif = document.querySelector('this.name');
                    // if(gif.classList.contains()){
                        gif.style.top = e.clientY + "px";
                        gif.style.left = e.clientX + "px";
                    // }
                    
                }
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
                // z-index: -1;
            }
    }
</style>