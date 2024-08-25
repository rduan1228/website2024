<script setup lang="ts"></script>

<script lang="ts">
import { defineComponent } from 'vue';

interface TimeRemaining {
  days: number;
  hours: number;
  minutes: number;
  seconds: number;
}

export default defineComponent({
  data() {
    return {
      timeRemaining: null as TimeRemaining | null,
      intervalId: null as number | null,
    };
  },
  mounted() {
    this.calculateTimeRemaining();
    this.intervalId = window.setInterval(this.calculateTimeRemaining, 1000);
  },
  beforeUnmount() {
    if (this.intervalId !== null) {
      clearInterval(this.intervalId);
    }
  },
  methods: {
    calculateTimeRemaining() {
      const targetDate = new Date('2024-10-18T19:00:00-05:00'); // Central Time (CT)
      const now = new Date();
      const difference = targetDate.getTime() - now.getTime();

      if (difference > 0) {
        const days = Math.floor(difference / (1000 * 60 * 60 * 24));
        const hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((difference % (1000 * 60)) / 1000);

        this.timeRemaining = { days, hours, minutes, seconds };
      } else {
        this.timeRemaining = null;
        if (this.intervalId !== null) {
          clearInterval(this.intervalId);
        }
      }
    },
  },
});
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
            <div class="time" v-if="timeRemaining">
                <div class="days">
                    <div class="time-value">{{ timeRemaining.days }}</div>
                    <div class="time-label">days</div>
                </div>
                <div class="hours">
                    <div class="time-value">{{ timeRemaining.hours }}</div>
                    <div class="time-label">hours</div>
                </div>
                <div class="minutes">
                    <div class="time-value">{{ timeRemaining.minutes }}</div>
                    <div class="time-label">minutes</div>
                </div>
                <div class="seconds">
                    <div class="time-value">{{ timeRemaining.seconds }}</div>
                    <div class="time-label">seconds</div>
                </div>
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
    border-bottom: solid 0.25vw black;
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
    border-left: solid 0.25vw black;
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
    font-size: xx-large;
}

.time div {
    height: 10vw; 
    width: 9vw;
    background-color: #E0DDB7;
    border: 1px solid black;
}

.days{
    margin-top: 2vw;
    display: flex;
    flex-direction: column;
}

.hours{
    margin-top: 3vw;
    display: flex;
    flex-direction: column;
}

.minutes{
    margin-top: 2vw;
    display: flex;
    flex-direction: column;
}

.seconds{
    margin-top: 4vw;
    display: flex;
    flex-direction: column;
}

.time .time-value {
    flex: 4;
    display: flex;
    align-items: center;
    justify-content: center;
    border: none;
    font-size: 3.5vw;
    font-family: 'pf-videotext';
    
}

.time .time-label {
    flex: 1;
    font-size: 1.5vw;
    text-align: right;
    padding-right: 0.5vw;
    box-sizing: border-box;
    border: none;
    font-family: 'open-sans';
}




</style>
 