<template>
<div id="works">
    <section>
        <h2>WORKS</h2>
        <div class="work-wrapper" v-for="work in works" :key="work.id">
            <div class="work-img-container">
                <h3 class="work-title animate">{{work.title}}</h3>
                <a :href="work.link" target="_blank">
                    <img class="work-img tilt" :src="'/static/work/' + work.img" :alt="work.title" data-tilt data-tilt-scale="1.05">
                </a>
            </div>
            <div class="work-description animate">
                <p>{{work.description}}</p>
                <ul >
                    <li v-for="tech in work.tech" :key="tech">#{{tech}}</li>
                </ul>
                
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
                    title: 'GROUPOMANIA',
                    img: 'miniature-groupomania.jpg',
                    description: 'Fullstack project of a corporate social network. With the creation of a secure API and storage in a database of the various articles written by users. Creation of the front-end interface with display and modification of articles.',
                    tech: ['VUEJS','NODEJS','EXPRESS','MYSQL','API'],
                    link:'https://github.com/imTho/Projet07-Groupomania'
                },

                {   
                    id : '2',
                    title: 'VACARMES',
                    img: 'miniature-vacarmes.jpg',
                    description: 'Website for press articles, produced in association with journalists students. Collaborative work with a team of 4 developers and 3 graphic designers.',
                    tech: ['HTML','SCSS','JS','GIT'],
                    link: 'http://cuej.info/mini-sites/armes/menu.html'
                },

                {   
                    id : '3',
                    title: 'ORINOCO',
                    img: 'miniature-orinico.jpg',
                    description: 'Creation and implementation of the front-end interface for an e-commerce website. Retrieval and display of products from an API and creation of the shopping cart management system.',
                    tech: ['HTML','SCSS','JS','GIT','API'],
                    link: 'https://github.com/imTho/Projet05-Orinoco'
                },

                {   
                    id : '4',
                    title: 'RULANTICA',
                    img: 'miniature-rulantica.jpg',
                    description: 'Proposal mock-up of a landing page for the Rulantica theme park website. Realization of the desktop and mobile versions.',
                    tech: ['ILLUSTRATOR','PHOTOSHOP']
                },

                
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
    margin-top: 30%;
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
    margin-bottom: 15%;
}

.work-img-container{
    position: relative;
    width: 50%;

        img{
            width: 100%;
            height: auto;
        }

        h3{
            word-wrap: wrap;
            text-shadow: 3px 3px 15px rgba(0, 0, 0, 0.384);
            position: absolute;
            bottom: 0;
            padding-left: 5rem;
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

    ul{
        flex-wrap: wrap;
        padding: 0;
        margin: 0;
        text-align: center;
        display: flex;
    }

    li{
        margin: 0;
        margin-left: 1vw;
        font-size: 1.35vw;
    }

    li:nth-child(1){
        margin-left: 0;
    }

    
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
            padding-left: 0;
            left: 0;
            font-size: 10vw;
        }
    }

    .work-description{
        margin-top: 2.5rem;
        width: 100%;
        font-size: 1.2rem;

        li{
            font-size: 1.2rem;
        }
    }
}
</style>