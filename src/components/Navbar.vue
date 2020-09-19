<template>
    <nav>
        <div class="nav-logo">
            <a href="">
                 <img src="../assets/logo.svg" alt="">
            </a>  
        </div>
        <ul class="nav-items">
            <li class="nav-item"> <a href="">work</a> </li>
            <li class="nav-item"> <a href="">about</a> </li>
        </ul>
        <div class="nav-socials">
            <div class="social-icon-container"> <a href="https://github.com/imTho" target="_blank"><img src="../assets/socials-media/github-brands.svg" alt=""></a> </div>
            <div class="social-icon-container"> <a href="https://www.linkedin.com/in/th%C3%A9o-eschlimann/" target="_blank"><img src="../assets/socials-media/linkedin-in-brands.svg" alt=""></a> </div>
            <div class="social-icon-container"> <a href="mailto:theo.eschlimann@gmail.com" target="_blank"><img src="../assets/socials-media/envelope-solid.svg" alt=""></a> </div>
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
    padding: 50px;
}

.nav-logo{ 
    height: 140px;

    img{
        height: 100%;
        width: auto;
    }
}

.nav-items{
    display: flex;
    padding: 0;
    margin: 0;
    flex-direction: columns;
    writing-mode: vertical-lr;
    font-size: 20px;
    margin-top: 30px;

    .nav-item{
        margin-top: 80px;
    }

    .nav-item a:hover{
        color: rgb(88, 88, 88);
    }

}
.nav-socials{
    display: flex;
    align-items: center;
    flex-direction: column;
    margin-top: 100px;

    .social-icon-container{
        margin-top: 25px;
        width: 25px;
        height: 25px;   
    }

    .social-line{
        margin-top: 35px;
        height: 100px;
        width: 2px;
        background-color: black;
    }

}

</style>