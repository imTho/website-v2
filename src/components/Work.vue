<template>
<div id="work">
    <section>

        <div class="work-wrapper">
            <div class="work-img-container">
                <h3 class="work-title">RULANTICA</h3>
                <img class="work-img" src="../assets/work/miniature-rulantica.jpg" alt="" data-tilt data-tilt-scale="1.05">
            </div>
            <div class="work-description">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed malesuada sapien in efficitur auctor. Nulla vitae ante sapien. Vestibulum nec lacus condimentum, aliquam purus sodales, porttitor elit. Etiam feugiat eget ligula vitae vehicula.
            </div>
        </div>

    </section>
</div>
</template>

<script>
import VanillaTilt from 'vanilla-tilt';

export default {
    name: 'Work',

    mounted(){

    VanillaTilt.init(document.querySelectorAll(".work-img"), {
        max: 5,
        speed: 200
    });

    },

    methods:{

    }
}
</script>

<style scoped lang="scss">
#work{
    margin-top: 9rem;
}

.work-wrapper{
    display: flex;
    width: 100%;
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
            cursor: default;

        }
}

.work-description{
    width: 50%;
    padding: 5%;
    font-size: 1.35vw;
    line-height: 170%;
    cursor: default;
}

@media (max-width: 1000px) {
    .work-wrapper{
        flex-direction: column;
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