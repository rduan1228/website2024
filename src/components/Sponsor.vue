<script setup lang="ts"></script>

<template>
    <div class="sponsor-parent">
        <div class="sponsor-left">
            <div class="star-sponsor-img"></div>
            <div class="star-title">STAR</div>
            <div class="sponsor-list">
                Coming soon...
            </div>
        </div>
        <div class="sponsor-right">
            <div class="sponsor-title">SPONSORS</div>
            <div class="celestial-title">CELESTIAL</div>
            <div class="sponsor-list">
                Coming soon...
            </div>
        </div>
    </div>
    
</template>

<style scoped>
.sponsor-parent{
    display: flex;
    height: 100vh;
    border-bottom: 0.5vh solid black;
}
.sponsor-left{
    flex: 38%;
    display: flex;
    flex-direction: column;
    height: 100%;
}

.sponsor-right{
    border-left: 0.25vw solid black;
    flex: 62%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.star-sponsor-img{
    height: 22vh;
    width: 15vw;
    margin-left: 1.5vw;
    margin-top: 4.4vh;
    background-color: rgb(195, 163, 226);
}

.star-title{
    font-size: 3.5vw;
    margin-top: 4vh;
    margin-bottom: 1vw;
    font-family: pf-videotext;
    justify-content: center;
    text-align: center;
}

.star-sponsor-list{
    display: grid;
    grid-template-columns: auto;
    width: 100%;
    text-align: left;
    margin-left: 1.5vw;
    margin-top: 5.8vh;
}

.sponsor-title{
    position: absolute;
    width: 8.9vw;
    font-size: 6.3vw;
    writing-mode: vertical-lr;
    height: 100%;
    text-align: left;
    margin-top: 3.8vh;
    font-family: pf-videotext;
    opacity: 0.5;
    left: 36.5%;

}

.celestial-sponsors{
    display: flex;
    flex-direction: column;
}

.celestial-title{
    font-size: 3.5vw;
    margin-top: 10.5vh;
    font-family: pf-videotext;
    text-align: center;
    width: 100%;
}

.sponsor-list{
    display: grid;
    grid-template-columns: auto;
    width: 100%;
    text-align: left;
    margin-left: 30.7%;
    margin-top: 5.8vh;
    font-family: open-sans;
    font-size: 1vw;
}

</style>
