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
  <div class="apply-parent">
    <img id="apply-leaves-1" src="/src/assets/leaves-2.png" />
    <img id="apply-leaves-2" src="/src/assets/leaves-2.png" />
    <h1 id="apply-text-1">COMING SOON</h1>
    <img class="apply-line" src="/src/assets/line-1.png" />
    <img class="apply-star" src="/src/assets/star-1.png" />

    <div class="apply-time-till" v-if="timeRemaining">
      <p class="apply-time-unit">{{ timeRemaining.days }}</p>
      <p class="apply-time-unit">{{ timeRemaining.hours }}</p>
      <p class="apply-time-unit">{{ timeRemaining.minutes }}</p>
      <p class="apply-time-unit">{{ timeRemaining.seconds }}</p>
      <p>
        <div class="apply-time-unit-2">days</div>
      </p>
      <p>
        <div class="apply-time-unit-2">hours</div>
      </p>
      <p>
        <div class="apply-time-unit-2">minutes</div>
      </p>
      <p>
        <div class="apply-time-unit-2">seconds</div>
      </p>
    </div>

    <a href="https://wustl.az1.qualtrics.com/jfe/form/SV_1YusN9NvNukt3ZY">
      <div class="apply-apply-now">
          <img src="/src/assets/yellowRectangle.png" />
          <h1 id="apply-text-2">apply now</h1>
      </div>
    </a>
  </div>
</template>

<style scoped>
#apply-text-2 {
  position: absolute;
  z-index: 100;
  color: #2b1853;
  font-family: 'spartan';
  font-size: 3vw;
}

.apply-apply-now {
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  width: 18vw;
  height: 8vw;
  left: 41vw;
  top: 38.5vw;
}

.apply-time-unit-2 {
  font-size: 1.75vw;
  font-family: 'spartan';
  display: flex;
  justify-content: center;
  align-items: center;
}

.apply-time-unit {
  display: flex;
  justify-content: center;
  align-items: center;
}

.apply-time-till {
  justify-content: space-between;
  width: 50vw;
  font-family: 'spartan-bold';
  font-size: 5.5vw;
  position: absolute;
  top: 27vw;
  left: 26vw;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(2, 1fr);
}

.apply-line {
  position: absolute;
  height: 0.125vw;
  width: 56vw;
  top: 24vw;
  left: 22vw;
}

.apply-star {
  position: absolute;
  height: 3.5vw;
  width: 3.5vw;
  top: 22vw;
  left: 49vw;
}

#apply-text-1 {
  position: absolute;
  font-family: 'FancyFont', serif;
  font-size: 5.7vw;
  width: 50vw;
  left: 24vw;
  top: 16vw;
}

#apply-leaves-2 {
  transform: scaleX(-1);
  position: absolute;
  width: 48vw;
  height: 34vw;
  left: 52vw;
}

#apply-leaves-1 {
  position: absolute;
  width: 48vw;
  height: 34vw;
}

.apply-parent {
  position: relative;
  height: 54vw;
  display: flex;
  width: 100vw;
}
</style>
