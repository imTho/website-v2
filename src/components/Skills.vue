<template>
  <div id="Skills">
      <section>
        <p>All my works are made with 💙 and :</p>
            <div class="skills-container">
                <span class="skills-item animate">#HTML</span>
                <span class="skills-item animate">#CSS</span>
                <span class="skills-item animate">#JS</span>
                <span class="skills-item animate">#SASS</span>
                <span class="skills-item animate">#GIT</span>
                <span class="skills-item animate">#NPM</span>
                <span class="skills-item animate">#VUE.JS</span>
                <span class="skills-item animate">#NODE.JS</span>
                <span class="skills-item animate">#EXPRESS</span>
                <span class="skills-item animate">#MONGODB</span>
                <span class="skills-item animate">#MYSQL</span>
                <span class="skills-item animate">#PHOTOSHOP</span>
                <span class="skills-item animate">#XD</span>
                <span class="skills-item animate">#ILLUSTRATOR</span>
                <span class="skills-item animate">#FIGMA</span>
            </div>
        </section>
    </div>
</template>

<script>
export default {
    name: 'Skills',
}
</script>

<style scoped lang="scss">
    #Skills{
        margin-top: 25rem;
    }

    p{
        font-size: 7vw;
        line-height: 140%;
        font-weight: 700;
        margin-bottom: 7.5rem;
    }

    .skills-container{
        display: flex;
        flex-wrap: wrap;
        overflow: hidden;
    }

    .skills-item{
        margin: 0rem 1rem 0rem 1rem;
        font-weight: bold;
        color: rgba(212, 212, 212, 0.699);
        font-size: 6vw;
        line-height: 100%;
        cursor: pointer;
        transition-duration: 0.5s;
        background: none;
    }

    .skills-item:hover{
        transform: scale(1.1);
        background: -webkit-gradient(linear,40% 0%, 75% 84%, from(#83d2ff), to(#0645AD), color-stop(.6,#8a68e6));
        background-clip: text;
        -webkit-text-fill-color: transparent; 
    }

    @media (max-width: 1000px) {
        #Skills{
            margin-top: 7rem;
        }
    }
</style>