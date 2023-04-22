<template>
  <div class="text-box">
    <h2>Text</h2>
    <slot></slot>
  </div>
</template>


<style scoped>
.text-box {
    margin: 0 auto;
    background-color: rgba(0, 0, 0, 0.6);
    height: 100%;
    width: 100%;
    z-index: 0;
    align-items: center;
}

.text-box > h2 {
    color: white;
    padding: 1vh;
    margin : 0;
    text-align: center;
    position: relative;
    top: 30%;
}
</style>