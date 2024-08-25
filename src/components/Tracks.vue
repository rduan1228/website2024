<script setup lang="ts"></script>

<template>
<div class="tracks">
  <div class="left-body">
    <div class="select-text">
      <h1>CHOOSE YOUR CHARACTER</h1>
      <p>Discover your preferred difficulty level + class.</p>
    </div>
    <div class="difficulty">
      <div class="emerging">
        <div class="d">
          <p class="star">*</p>
          <p class="level">(level 1)</p>
        </div>
        <div>
          <h1>EMERGING</h1>
          <p>Gather 0-2 years of experience or hackathons.</p>
        </div>
      </div>
      <div class="master">
        <div class="d">
          <p class="star">***</p>
          <p class="level">(level 3)</p>
        </div>
        <div>
          <h1>MASTER</h1>
          <p>Unlock 3+ years of experience or hackathons.</p>
        </div>
      </div>
    </div>
    <div class="class">
      <div class="ai center">
        <div class="c"></div>
        <p>ARTIFICIAL INTELLIGENCE</p>
      </div>
      <div class="visuals center">
        <div class="c"></div>
        <p>VISUALLY STUNNING</p>
      </div>
      <div class="health center">
        <div class="c"></div>
        <p>HEALTH & FITNESS</p>
      </div>
    </div>
  </div>
  <div class="right-body">
    <h1>TRACKS</h1>
  </div>
</div>
</template>

<style scoped>
.tracks {
  display: flex;
  justify-content: space-between;
  height:150vh;
  border-bottom: 0.25vw solid black;
}

.left-body {
  padding-left: 12.75vw;
  padding-top: 15vh;
  width: 82.5%;
  height: auto;   
}

.select-text h1{
  font-family: 'pf-videotext';
  font-size: 3.175vw;
  font-weight: 400;
}

.select-text p{
  padding-top: 4vh;
  padding-left: 0.25vw;
  font-family: 'open-sans';
  font-size: 1vw;
  font-weight: 400;
}

.difficulty {
  display: flex;
  justify-content: space-between;
  padding-top: 10vh;
  padding-right: 19vw;
}

.d{
  height: 33vh;
  width: 23.75vw;
  background-color: rgba(185, 163, 213, 0.5);
  text-align: right;
}

.emerging .star{
  padding-right: 0.25vw;
  font-family: 'Helvetica';
  font-size: 6vw;
  font-weight: 400;
}

.emerging .level{
  padding-top: 17.5vh;
  padding-right: 0.5vw;
  font-family: 'pf-videotext';
  font-size: 1.3vw;
  font-weight: 400;
}

.master .star{
  padding-right: 0.25vw;
  font-family: 'Helvetica';
  font-size: 6vw;
  font-weight: 400;
}

.master .level{
  padding-top: 17.5vh;
  padding-right: 0.5vw;
  font-family: 'pf-videotext';
  font-size: 1.3vw;
  font-weight: 400;
}

.d:hover {
  transition: ease-in-out 0.5s;
  background-color: #64D3F5;
}

.difficulty h1 {
  padding-top: 3vh;
  font-family: 'pf-videotext';
  font-size: 1.75vw;
  font-weight: 400;
}

.difficulty p {
  padding-top: 0.5vh;
  font-family: 'open-sans';
  font-size: 1vw;
  font-weight: 400;
}

.class {
  display: flex;
  justify-content: space-between;
  padding-top: 9vh;
  padding-right: 13vw;
}

.c{
  height: 37vh;
  width: 17.25vw;
  background-color: rgba(185, 163, 213, 0.5);
  display: flex;
  flex-direction: column;
  align-items: center ;
}

.c:hover {
  transition: ease-in-out 0.5s;
  background-color: #64D3F5;
}

.class p {
  padding-top: 3vh;
  font-family: 'pf-videotext';
  font-size: 1.25vw;
  font-weight: 400;
}

.center {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.right-body {
  width: 17.5%;
  height: auto;
  border-left: 0.25vw solid black;
} 

.right-body h1 {
  font-family: 'pf-videotext';
  font-size: 6vw;
  color: rgba(0, 0, 0, 0.5);
  transform: rotate(90deg);
  transform-origin: 0 0;
  display: inline-block;
  margin-top :2vh;
  margin-left: 4.5vw;
  font-weight:400;
}

</style>
