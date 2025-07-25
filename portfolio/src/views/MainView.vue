<script setup>
import MouseBounce from '../components/MouseBounce.vue'
import PortFolioConnect from '@/components/PortfolioConnect.vue'
import SideNavigation from '@/components/SideNavigation.vue'
import ProjectDescribe from '@/components/ProjectDescribe.vue'
import ProjectImage from '@/components/ProjectImage.vue'
import ContectModal from '@/components/ContectModal.vue'

import { onUnmounted, ref, watch } from 'vue'

const showModal = ref(false)

const toggleModal = () => {
  showModal.value = !showModal.value
  console.log(showModal.value)
}

watch(showModal, (newVal) => {
  if (newVal) {
    document.body.style.overflow = 'hidden'
  } else {
    document.body.style.overflow = ''
  }
})

onUnmounted(() => {
  document.body.style.overflow = ''
})
</script>

<template>
  <main>
    <section class="sloganContainer">
      <div class="sloganWrapper">
        <h1 class="sloganTitle">
          문제를 해결하고<br />
          가능성을 연결 하는
        </h1>
        <p class="sloganContent">프론트 엔드 <span>개발자 이준호</span> 입니다</p>
      </div>
    </section>
    <section class="projectContainer">
      <div class="projectWrapper">
        <ProjectDescribe />
        <ProjectImage />
      </div>
    </section>
    <section class="devtoolsContainer">
      <div class="devtoolsWrapper">
        <h2 class="devtoolsTitle">기술 스택 및 도구</h2>
        <p class="devtoolsDescription">아래의 기술 역량을 가지고 있으며 활용할 수 있습니다.</p>
        <div class="devtoolsButtons">
          <button class="active">프론트 엔드</button>
          <button>라이브러리</button>
          <button>환경 및 배포</button>
        </div>
        <div class="devtoolsImagesWrapper">
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
          <div class="devtoolsImagesitem"></div>
        </div>
      </div>
    </section>
    <MouseBounce />
    <PortFolioConnect :toggleModal="toggleModal" />
    <SideNavigation />
    <ContectModal :toggleModal="toggleModal" :showModal="showModal" />
  </main>
</template>
<style scoped>
main {
  width: 100%;
  height: fit-content;
}
.sloganContainer {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  cursor: default;
}
.sloganWrapper {
  display: flex;
  width: 100%;
  flex-direction: column;
  align-items: center;
  gap: 60px;
  justify-content: center;
  margin: 0 auto;
}
.sloganTitle {
  color: #333;
  font-size: 48px;
  text-align: center;
  font-weight: bold;
}
.sloganContent {
  color: #a2a2a2;
  font-size: 32px;
  font-weight: bold;
}
.sloganContent > span {
  font-weight: bold;
  color: #333;
}
.projectContainer {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: default;
}
.projectWrapper {
  width: fit-content;
  display: flex;
  align-items: center;
  gap: 90px;
}
.devtoolsContainer {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: default;
}
.devtoolsWrapper {
  width: 600px;
  height: fit-content;
}
.devtoolsTitle {
  text-align: center;
  font-size: 20px;
  font-weight: bold;
  color: #1387fa;
  margin-bottom: 5px;
}
.devtoolsDescription {
  text-align: center;
  font-size: 24px;
  font-weight: bold;
  color: #000;
  margin-bottom: 64px;
}
.devtoolsButtons {
  width: fit-content;
  background-color: #eee;
  border-radius: 20px;
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  padding: 5px;
  margin-bottom: 25px;
}
.devtoolsButtons > button {
  padding: 7px 16px;
  border-radius: 20px;
  border: none;
  color: #a5a3a3;
  background-color: transparent;
  font-weight: 900;
  font-size: 16px;
  cursor: pointer;
}
.devtoolsButtons > button.active {
  background-color: #fff;
  color: #000;
}
.devtoolsImagesWrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 480px;
  gap: 20px;
  margin: 0 auto;
}
.devtoolsImagesitem {
  width: 60px;
  height: 60px;
  background-color: #a5a3a3;
  border-radius: 5px;
  cursor: pointer;
}
</style>
