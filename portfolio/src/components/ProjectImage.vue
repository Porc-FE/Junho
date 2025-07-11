<script setup></script>
<template>
  <div class="imageContainer">
    <div></div>
    <div></div>
    <div></div>
  </div>
</template>
<style scoped>
.imageContainer {
  width: 640px;
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}
.imageContainer > div {
  height: 255px;
  background-color: #e5f5ff;
  cursor: pointer;
}
.imageContainer > div:nth-child(1) {
  width: calc(50% - 10px);
  border-radius: 30px 0 30px 0;
}
.imageContainer > div:nth-child(2) {
  width: calc(50% - 10px);
  border-radius: 100px;
}
.imageContainer > div:nth-child(3) {
  width: 100%;
  border-bottom-right-radius: 20px;
}
</style>
