<template>
  <div>

    <div class="footer-wrapper">
        <div class="footer-line">
          Looking for a web-developer to hire ? <br>
          I'm in ! Contact me -> 
        </div>
        
        <ul class="footer-contact">
            <li><a href="mailto:theo.eschlimann@gmail.com" target="_blank"><span>Email :</span>  theo.eschlimann@gmail.com</a></li>
            <li><a href="https://www.linkedin.com/in/th%C3%A9o-eschlimann/" target="_blank"><span>LinkedIn :</span> Théo-Eschlimann</a></li>
            <li><a href="https://github.com/imTho" target="_blank"><span>GitHub :</span> imTho</a></li>
        </ul>
    </div>
    
    <div class="copyright"> Made by <strong>Théo Eschlimann</strong> - Copyright 2020</div>
  </div>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style scoped lang="scss">
    .footer-wrapper{
        display: flex;
        justify-content: space-between;
        margin-top: 13rem;
        font-size: 1.5vw;
    }

    .footer-line{
        display: flex;
        flex-direction: column;
    }

    .footer-contact{
        text-align: right;
        font-size: 1.2rem;

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

    .copyright{
        margin: 2rem 0rem 2rem 0rem;
        font-size: 1rem;
    }

    @media (max-width: 1000px) {
        .footer-wrapper{
            flex-direction: column;
            margin-top: 7rem;
            font-size: 1.5rem;
        }

        .footer-contact{
            text-align: left;
            font-size: 1rem; 
            padding: 0;
        }
    }

</style>