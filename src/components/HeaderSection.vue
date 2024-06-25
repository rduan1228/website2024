<script setup lang="ts"></script>

<template>
    <div class="header-parent">
        <a id="mlh-trust-badge" style="position: absolute;;max-width:100px;min-width:60px;right:1vw;top:0;width:10%;z-index:10000" href="https://mlh.io/na?utm_source=na-hackathon&utm_medium=TrustBadge&utm_campaign=2025-season&utm_content=white" target="_blank"><img src="https://s3.amazonaws.com/logged-assets/trust-badge/2025/mlh-trust-badge-2025-white.svg" alt="Major League Hacking 2025 Hackathon Season" style="width:100%"></a>
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
    left: 80vw;
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
 