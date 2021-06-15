<template>
    <header>
        <!--span><img src="../assets/branch.png" alt="" class="left"></span-->
        <nav>
            <a href="#home" @click.prevent="link">Hem</a>
            <a href="#about" @click.prevent="link">Om bröllopet</a>
            <a href="#program" @click.prevent="link">Program</a>
            <a href="#accommodation" @click.prevent="link">Boende & Transport</a>
            <a href="#clothing" @click.prevent="link">Klädsel</a>
            <a href="#osa" @click.prevent="link">Osa</a>
        </nav>
         <!--span><img src="../assets/branch.png" alt=""></span-->
    </header>
    <div class="wave">
        <!--svg viewBox="0 0 1210 50" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><path fill="rgba(255, 255, 255, 0.5)" d="M 0 0 C 93.5 0 93.5 18 187 18 L 187 18 L 187 0 L 0 0 Z" stroke-width="0"></path> <path fill="rgba(255, 255, 255, 1)" d="M 186 18 C 283.5 18 283.5 4 381 4 L 381 4 L 381 0 L 186 0 Z" stroke-width="0"></path> <path fill="rgba(255, 255, 255, 1)" d="M 380 4 C 516.5 4 516.5 31 653 31 L 653 31 L 653 0 L 380 0 Z" stroke-width="0"></path><path fill="rgba(255, 255, 255, 1)" d="M 652 31 C 764 31 764 4 876 4 L 876 4 L 876 0 L 652 0 Z" stroke-width="0"></path><path fill="rgba(255, 255, 255, 1)" d="M 875 4 C 969.5 4 969.5 19 1064 19 L 1064 19 L 1064 0 L 875 0 Z" stroke-width="0"></path><path fill="rgba(255, 255, 255, 1)" d="M 1063 19 C 1136.5 19 1136.5 0 1210 0 L 1210 0 L 1210 0 L 1063 0 Z" stroke-width="0"></path></svg-->
    </div>
</template>

<script setup>
    function link (event) {
        
        document.querySelector(event.target.hash).scrollIntoView({ 
            behavior: 'smooth' 
        });
         
    }
</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-around;
        align-items: center;
        background: var(--transparent);
        height: var(--header);
    }

    /*img.left {
       transform: rotateX(60deg);
    }

    img.right {
        transform: rotateY(180deg);
        border: 1px solid red
    }*/

    .wave {
        display: block;
        position: relative;
        top: -2px;
        height: 50px;
        background-image: url('data:image/svg+xml;utf8,<svg viewBox="0 0 1210 50" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><path fill="rgba(255, 255, 255, 1)" d="M 0 0 C 93.5 0 93.5 18 187 18 L 187 18 L 187 0 L 0 0 Z" stroke-width="0"></path> <path fill="rgba(255, 255, 255, 1)" d="M 186 18 C 283.5 18 283.5 4 381 4 L 381 4 L 381 0 L 186 0 Z" stroke-width="0"></path> <path fill="rgba(255, 255, 255, 1)" d="M 380 4 C 516.5 4 516.5 31 653 31 L 653 31 L 653 0 L 380 0 Z" stroke-width="0"></path><path fill="rgba(255, 255, 255, 1)" d="M 652 31 C 764 31 764 4 876 4 L 876 4 L 876 0 L 652 0 Z" stroke-width="0"></path><path fill="rgba(255, 255, 255, 1)" d="M 875 4 C 969.5 4 969.5 19 1064 19 L 1064 19 L 1064 0 L 875 0 Z" stroke-width="0"></path><path fill="rgba(255, 255, 255, 1)" d="M 1063 19 C 1136.5 19 1136.5 0 1210 0 L 1210 0 L 1210 0 L 1063 0 Z" stroke-width="0"></path></svg>');
        background-size: cover;
        background-repeat: no-repeat;
    }

    @media (max-width:1209px) {
        .wave {
            background-size: contain;
        }
    }


    a {
        padding: 0 20px;
    }
</style>