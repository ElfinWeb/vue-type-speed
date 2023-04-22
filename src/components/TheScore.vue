<template>
  <div class="score-board">
    <h3>SCORE : 0<span class="current-score"></span></h3>
  </div>
</template>

<style scoped>
.score-board {
  margin: 0 auto;
  margin-bottom: 1%;
  background-color: rgba(245, 237, 237, 0.938);
  border-radius: 2vh;
  padding: 1vh;
  box-shadow: 0vh 0vh 1vh 1vh rgba(0, 0, 0, 0.541);
  width: 10%;
  display:flex;
}

.score-board > h3 {
  margin: 0;
  color: rgb(0, 0, 0);
}
</style>
