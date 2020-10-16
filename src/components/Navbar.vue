<template>
    <nav>
        <div class="nav-socials">
            <div class="social-icon-container"> <a href="https://github.com/imTho" target="_blank" title="GitHub profil"><img src="../assets/socials-media/github-brands.svg" alt="GitHub icon"></a> </div>
            <div class="social-icon-container"> <a href="https://www.linkedin.com/in/th%C3%A9o-eschlimann/" target="_blank" title=" LinkedIn profil"><img src="../assets/socials-media/linkedin-in-brands.svg" alt="LinkedIn icon"></a> </div>
            <div class="social-icon-container"> <a href="mailto:theo.eschlimann@gmail.com" target="_blank" title="Send mail"><img src="../assets/socials-media/envelope-solid.svg" alt="Email icon" ></a> </div>
        </div>

        <div class="nav-logo">
            <a href="#">
                 <img class="logo" src="../assets/logo-mask2.svg" alt="logo">
                 <img class="logo-gradient" src="../assets/logo-gradient.webp" alt="logo-gradient">
            </a>  
        </div>

        <ul class="nav-items">
            <li class="nav-item"> <a href="#">#works</a> </li>
            <li class="nav-item"> <a href="#">#skills</a> </li>
        </ul>    
    </nav>
</template>

<script>
export default {
    name: 'Navbar'
}
</script>

<style scoped lang="scss">
nav{
    position: fixed;
    left: 0;
    top: 0;
    display: flex;
    align-items: center;
    justify-content: space-around;
    width: 100%;
    background-color: rgba(255, 255, 255, 0.9);
    z-index: 50;
}

.nav-logo{ 
    position: relative;
    width: 9rem;
    height: 9rem;

    .logo-gradient, .logo{
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0; 
    }

    .logo-gradient{
        z-index: -1;
    }
}

.nav-items{
    display: flex;
    font-size: 1.25rem;
    padding: 0;
    padding-inline-start: 0px;
    transition-duration: 0.2s;
    
    li{
        margin: 1rem;
    }

    .nav-item a:hover{
        color: rgb(88, 88, 88);
    }
}

.nav-socials{
    display: flex;
    align-items: center; 

    .social-icon-container{
        margin: 1rem;
    }

    img{
        height: 1.7rem;
        width: 1.7rem;
    }

    .social-icon-container img:hover{
        transform: scale(1.15);
        transition: all 0.2s ease;
    }
}

</style>