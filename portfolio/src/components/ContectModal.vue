<script setup>
const { toggleModal, showModal } = defineProps({
  showModal: Boolean,
  toggleModal: Function,
})
</script>
<template>
  <section v-if="showModal" @click="toggleModal" class="modalContainer">
    <div class="modalWrapper">
      <h1>Connect with Me</h1>
      <div class="modalBox">
        <div class="modalItem"><p>깃허브</p></div>
        <div class="modalItem">
          <p>이메일</p>
        </div>
        <div class="modalItem">
          <p>블로그</p>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
.modalContainer {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.4);
  backdrop-filter: blur(5px);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 100;
}
.modalWrapper {
  width: 520px;
  height: 300px;
  display: flex;
  flex-direction: column;
  gap: 40px;
  padding-top: 44px;
  align-items: center;
  background-color: #fff;
  border-radius: 3px;
  box-shadow: 0 2px 4p rgba(0, 0, 0, 1);
}
.modalWrapper h1 {
  font-weight: bold;
  font-size: 24px;
  color: #1387fa;
}
.modalBox {
  width: fit-content;
  height: fit-content;
  display: flex;
  gap: 10px;
}
.modalItem {
  width: 150px;
  height: 150px;
  border-radius: 5px;
  background-color: #f1f1f1;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}
.modalItem:hover {
  z-index: 10;
  transform: scale(1.05);
  transition: 0.2s linear;
}
</style>
