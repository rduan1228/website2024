<script setup lang="ts"></script>

<template>
<div class="contact-parent">
    <img id="contact-leaves-1" src="/src/assets/leaves-2.png"/>
    <img id="contact-leaves-2" src="/src/assets/leaves-2.png"/>
    <a href="https://www.instagram.com/hackwashu/?hl=en"><img id="contact-insta" src="/src/assets/insta.png"></a>
    <a href="https://www.linkedin.com/company/hack-washu"><img id="contact-linkedin" src="/src/assets/linkedin.png"></a>
    <a href="mailto:hackwashu@gmail.com"><img id="contact-gmail" src="/src/assets/gmail.png"></a>
    <h1 class="contact-text-1">CONTACT US</h1>
    <a href="https://www.instagram.com/hackwashu/?hl=en"><p class="contact-text-2">hackwashu</p></a>
    <a href="https://www.linkedin.com/company/hack-washu"><p class="contact-text-3">linkedin.com/company/hack-washu</p></a>
    <a href="mailto:organizers@hackwashu.com"><p class="contact-text-4">hackwashu at gmail.com</p></a>
</div>
</template>
 
<style scoped>

#contact-leaves-2{
    position: absolute;
    transform: scaleX(-1) scaleY(-1);
    right: 0vw;
    top: 20vw;
    width: 48vw;
    height: 32vw;

}

#contact-leaves-1{
    position: absolute;
    transform: scaleY(-1);
    top: 20vw;
    width: 48vw;
    height: 32vw;

}

.contact-text-4{
    position: absolute;
    font-family: 'spartan';
    font-size: 3vw;
    width: 100vw;
    left: 40vw;
    top: 34vw;
}

.contact-text-3{
    position: absolute;
    font-family: 'spartan';
    font-size: 3vw;
    width: 100vw;
    left: 40vw;
    top: 22vw;
}

.contact-text-2{
    position: absolute;
    font-family: 'spartan';
    font-size: 3vw;
    width: 100vw;
    left: 40vw;
    top: 10.75vw;
}

#contact-linkedin{
    position: absolute;
    height: 9vw;
    width: 9vw;
    left: 26.5vw;
    top: 19vw;
}

#contact-gmail{
    position: absolute;
    height: 7vw;
    width: 8vw;
    left: 26.8vw;
    top: 32vw;
}

#contact-insta{
    position: absolute;
    height: 12vw;
    width: 12vw;
    left: 25vw;
    top: 6vw;
}

.contact-text-1{
    position: absolute;
    width: 100vw;
    text-align: center;
    font-family: 'FancyFont';
    font-size: 4vw;
}

.contact-parent{
    position: relative;
    height: 55vw;
    display: flex;
    width: 100vw;
}


</style>
