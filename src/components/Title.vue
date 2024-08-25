<script setup lang="ts">
import Timer from "./Timer.vue";
</script>

<template>
    <div class="title">
        <div class="left-body">
            <div class="left-body-text">
                <h1>HACK <br> WASHU‘24</h1>
                <p>OCT 11-12</p>
            </div> 
            <div class="timer-text">
                <h2>THE <span class="big"> ADVENTURE </span> BEGINS IN </h2>
            </div>
            <div class="time">
                <div class="days"></div>
                <div class="hours"></div>
                <div class="minutes"></div>
                <div class="seconds"></div>
                <!-- <Timer /> -->
            </div>
        </div>
         <div class="right-body">
            <div class="scroll">
                <p> (SCROLL FOR INFO)</p>
                <img src="src/assets/arrow.png">
            </div>
         </div>
    </div>
</template>

<style scoped>

.title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 0 0 12vw;
    height: 97.5vh;
    border-bottom: solid 0.5vw black;
}

.left-body {
    display: flex;
    flex-direction: column;
    width: 65%;
    height: 100%;
    margin-top: 20vh;
}

.left-body-text h1 {
    font-size: 8.5vw;
    font-family: 'pf-videotext';
    color: black;
    font-weight: 400;
    line-height: 0.9;
}

.left-body-text p {
    font-size: 2vw;
    font-family: 'open-sans';
    color: black;
    font-weight: 400;
    padding-left: 0.75vw;
}

.timer-text {
    margin-left: 0.75vw;
    margin-right: 15vw;
    border-bottom: solid 0.3vw black;
}

.timer-text h2 {
    font-size: 2.25vw;
    font-family: 'pf-videotext';
    color: black;
    font-weight: 400;
    padding-top: 7vw;
}

.big {
    font-size: 3.5vw;
    color: black;
}

.right-body {
    width: 35%;
    height: 97.5vh;
    border-left: solid 0.5vw black;
}

.scroll{
    display: flex;
    align-items: center;
    flex-direction: column;
}

.scroll p{
    font-size: 1.75vw;
    font-family: 'pf-videotext';
    color: black;
    font-weight: 400;
    padding-top: 40vw;
    padding-left: 1vw;
}

.scroll img{
    height: 4vw;
    width: 3vw;
    padding-top: 1vw;
    padding-left: 1vw;
}

.time {
    display: flex;
    justify-content: space-between;
    margin-left: 0.75vw;
    margin-right: 15vw;
}

.time div {
    height: 10vw; 
    width: 9vw;
    background-color: #E0DDB7;
    border: 1px solid black;
}

.days{
    margin-top: 2vw;
}

.hours{
    margin-top: 3vw;
}

.minutes{
    margin-top: 2vw;
}

.seconds{
    margin-top: 4vw;
}




</style>
 