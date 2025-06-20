<script setup></script>
<template>
  <div class="navigationContainer">
    <div class="navigationWrapper">
      <div class="navigationItems"></div>
      <div class="navigationItems"></div>
      <div class="navigationItems"></div>
      <div class="navigationItems"></div>
    </div>
  </div>
</template>
<style scoped>
.navigationContainer {
  width: 26px;
  height: 163px;
  display: flex;
  justify-content: center;
  position: absolute;
  top: 50%;
  left: 20px;
  transform: translate(0, -50%);
}
.navigationWrapper {
  width: 1px;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  background-color: #999;
}
.navigationItems {
  cursor: pointer;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background-color: #e2e2e2;
}
</style>
