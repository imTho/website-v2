<template>
    <nav>
        <div class="nav-logo">
            <a href="#">
                 <img class="logo" src="../assets/logo-mask.svg" alt="logo">
                 <img class="logo-gradient" src="../assets/logo-gradient.webp" alt="logo-gradient">
            </a>  
        </div>
        <ul class="nav-items">
            <li class="nav-item"> <a href="#">work</a> </li>
            <li class="nav-item"> <a href="#">skills</a> </li>
        </ul>
        <div class="nav-socials">
            <div class="social-icon-container"> <a href="https://github.com/imTho" target="_blank" title="Profil GitHub"><img src="../assets/socials-media/github-brands.svg" alt="GitHub icon"></a> </div>
            <div class="social-icon-container"> <a href="https://www.linkedin.com/in/th%C3%A9o-eschlimann/" target="_blank" title="Profil LinkedIn"><img src="../assets/socials-media/linkedin-in-brands.svg" alt="LinkedIn icon"></a> </div>
            <div class="social-icon-container"> <a href="mailto:theo.eschlimann@gmail.com" target="_blank" title="Envoyer un mail"><img src="../assets/socials-media/envelope-solid.svg" alt="Email icon" ></a> </div>
            <div class="social-line"></div>
        </div>
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
    flex-direction: column;
    align-items: center;
    height: 100%;
    padding: 3.75rem 2.2rem 2.2rem 2.2rem;
}

.nav-logo{ 
    height: 8.75rem;
    width: 8.75rem;
    position: relative;
    margin-bottom: 2.8rem;

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
    padding: 0;
    margin: 0;
    flex-direction: columns;
    writing-mode: vertical-lr;
    font-size: 1.25rem;

    .nav-item{
        margin-top: 4.2rem;
    }

    .nav-item a:hover{
        color: rgb(88, 88, 88);
    }

}
.nav-socials{
    display: flex;
    align-items: center;
    flex-direction: column;
    margin-top: 5.8rem;

    .social-icon-container{
        margin-top: 1.56rem;
        width: 1.56rem;
        height: 1.56rem;  
         
    }
    
    .social-icon-container img:hover{
        transform: scale(1.1);
        transition: all 0.1s ease;
    }
    

    .social-line{
        margin-top: 2.18rem;
        height: 6.25rem;
        width: 0.125rem;
        background-color: black;
    }

}

</style>