<script setup></script>
<template>
  <div class="mouseContainer">
    <div class="mouseWrapper">
      <div class="mouseScroller"></div>
    </div>
  </div>
</template>
<style scoped>
.mouseContainer {
  width: 47px;
  height: 69px;
  display: flex;
  justify-content: center;
  padding: 9px;
  background-color: #efefef;
  border-radius: 30px;
  position: absolute;
  bottom: 10px;
  transform: translate(-50%, -50%);
  left: 50%;
}
.mouseWrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 30px;
  height: 30px;
  background-color: #fff;
  border-radius: 50%;
  animation: bounceUpDown 3s ease-in-out infinite;
}
.mouseScroller {
  width: 18px;
  height: 18px;
  border-radius: 50%;
  background-color: #e0e0e0;
}

@keyframes bounceUpDown {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(19px);
  }
  100% {
    transform: translateY(0);
  }
}
</style>
