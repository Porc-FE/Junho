<script setup>
import MouseBounce from '../components/MouseBounce.vue'
import PortFolioConnect from '@/components/PortfolioConnect.vue'
import SideNavigation from '@/components/SideNavigation.vue'
import ProjectDescribe from '@/components/ProjectDescribe.vue'
import ProjectImage from '@/components/ProjectImage.vue'
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
    <section></section>
    <MouseBounce />
    <PortFolioConnect />
    <SideNavigation />
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
</style>
