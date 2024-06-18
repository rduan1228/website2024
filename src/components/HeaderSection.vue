<script setup lang="ts"></script>

<template>
    <div class="header-parent">
        <img className="headerHackWashU" src="/src/assets/hackwashu.png"/>
        <img className="headerBear" src="/src/assets/headerBear.png"/>
        <!-- <div class="scrollLinks">
            <ul>
                <li>apply</li>
                <li>about</li>
                <li>division</li>
                <li>tracks</li>
                <li>contact us</li>
            </ul>
        </div> -->
    </div>

</template>

<style scoped>

.headerHackWashU{
    position: absolute;
    width: 46vw;
    height: 10vw;
}

.headerBear{
    position: absolute;
    width: 8vw;
    height: 8vw;
    /* left: 80vw; */
    left: 90vw;
    top: 2vw;
}

.header-parent{
    position: relative;
    display: flex;
    width: 100vw;
    height: 11vw;
}

li{
    margin-top: 0.5vw;
}

.scrollLinks{
    position: absolute;
    text-align: center;
    left: 90vw;
    height: 10vw;
    justify-content: space-around;
    top: 1.2vw;
    font-size: 1.4vw;
    font-family: 'spartan', sans-serif;
    width: 8vw;
    gap: 1vw;
}

</style>
