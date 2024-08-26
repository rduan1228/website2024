<script setup lang="ts"></script>

<template>
<div class="apply">
  <h1 class="title">FULFILL YOUR DESTINY.</h1>
  <div class="apply-button">APPLY NOW!!</div>
  <p>(PRESS TO START)</p>
</div>
</template>
 
<style scoped>
.apply {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 52vh;
  padding-top: 25vh;
}

.apply-button {
  background-color: #64D3F5;
  border: 0.2vw solid black;
  padding: 2.1vw 3vw 2.05vw 3vw;
  margin-top: 4vw;
  font-family: 'pf-videotext';
  font-size: 2.75vw;
}

.apply-button:hover {
  background-color: #C5D2CE;
  transition: ease-in 0.5s;
}

.title {
  font-family: 'pf-videotext';
  font-size: 4.25vw;
  color: black;
  font-weight: 400;
}

p {
  padding-top: 1.5vh;
  font-family: 'pf-videotext';
  font-size: 1.5vw;
  color: black;
}
</style>
