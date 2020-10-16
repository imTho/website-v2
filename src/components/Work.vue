<template>
<div id="works">
    <section>
        <h2>WORKS</h2>
        <div class="work-wrapper" v-for="work in works" :key="work.id">
            <div class="work-img-container">
                <h3 class="work-title animate">{{work.title}}</h3>
                <img class="work-img tilt" :src="'/static/work/' + work.img" :alt="work.title" data-tilt data-tilt-scale="1.05">
            </div>
            <div class="work-description animate">
                {{work.description}}
            </div>
        </div>

    </section>
</div>
</template>

<script>
import VanillaTilt from 'vanilla-tilt';

export default {
    name: 'Work',

    data(){
        return{
            works: [
                {   
                    id : '1',
                    title: 'RULANTICA',
                    img: 'miniature-rulantica.jpg',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed malesuada sapien in efficitur auctor. Nulla vitae ante sapien. Vestibulum nec lacus condimentum, aliquam purus sodales, porttitor elit. Etiam feugiat eget ligula vitae vehicula.'
                },

                {   
                    id : '2',
                    title: 'AMNEVILLE',
                    img: 'miniature-amneville.jpg',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed malesuada sapien in efficitur auctor. Nulla vitae ante sapien. Vestibulum nec lacus condimentum, aliquam purus sodales, porttitor elit. Etiam feugiat eget ligula vitae vehicula.'
                }
            ]
        }
    },

    mounted(){
        VanillaTilt.init(document.querySelectorAll(".tilt"), {
            max: 5,
            speed: 200
        });
    },

    methods:{

    }
}
</script>

<style scoped lang="scss">
#works{
    margin-top: 20rem;
}

h2{
    text-align: center;
    position: relative;
    top: -3rem;
    margin: 0;
    line-height: 0;
    color: rgba(243, 243, 243, 0.582);
    font-size: 20vw;
    z-index: -50;
}

.work-wrapper{
    display: flex;
    width: 100%;
    margin-bottom: 13rem;
}

.work-img-container{
    position: relative;
    width: 50%;

        img{
            width: 100%;
            height: auto;
        }

        h3{
            text-shadow: 3px 3px 15px rgba(0, 0, 0, 0.384);
            position: absolute;
            bottom: 0;
            right: -50%;
            margin: 0;
            line-height: 0;
            font-size: 9vw;
            z-index: 5;
            pointer-events: none;
            cursor: default;

        }
}

.work-description{
    width: 50%;
    padding: 5%;
    font-size: 1.35vw;
    line-height: 170%;
    cursor: default;
    z-index: -1;
}

@media (max-width: 1000px) {
    #works{
        margin-top: 12rem;
    }

    .work-wrapper{
        flex-direction: column;
        margin-bottom: 5rem;
    }
    .work-img-container{
        width: 100%;

        h3{
            left: 0;
        }
    }

    .work-description{
        margin-top: 2.5rem;
        width: 100%;
        font-size: 1.2rem;
    }
}

@media (max-width: 1250px) {

    .work-img-container{

        h3{
           font-size: 7rem; 
        }
    }
}
</style>