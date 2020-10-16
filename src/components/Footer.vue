<template>
  <div id="Footer">
      <div class="footer-line">
          Looking for a web-developer to hire ? <br>
          I'm in ! Contact me -> 

          <span>Théo Eschlimann - Copyright 2020</span> 
      </div>
      
        <ul class="footer-contact">
            <li><a href="mailto:theo.eschlimann@gmail.com" target="_blank"><span>Email :</span>  theo.eschlimann@gmail.com</a></li>
            <li><a href="https://www.linkedin.com/in/th%C3%A9o-eschlimann/" target="_blank"><span>LinkedIn :</span> Théo-Eschlimann</a></li>
            <li><a href="https://github.com/imTho" target="_blank"><span>GitHub :</span> imTho</a></li>
        </ul>
      
  </div>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style scoped lang="scss">
    #Footer{
        display: flex;
        justify-content: space-between;
        margin-top: 13rem;
        padding: 5rem 0rem 5rem 0rem;
        height: 20rem;
        width: 100%;
        font-size: 2vw;
    }

    .footer-line{
        display: flex;
        flex-direction: column;

        span{
            margin-top: 2rem;
            font-size: 1vw;
        }
    }

    .footer-contact{
        text-align: right;
        font-size: 1vw;

        li{
            transition-duration: 0.2s;
        }

        li:hover{
            padding-right: 1rem;
        }

        span{
            font-weight: bold;
        }
    }

</style>