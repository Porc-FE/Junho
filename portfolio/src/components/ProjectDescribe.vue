<script script></script>
<template>
  <article class="describeContainer">
    <div class="describeIcon"></div>
    <h2 class="describeTitle">React, 오픈 API를 활용한 프로젝트</h2>
    <p>사용자 정보 UI 개선 및 CRUD 기능 개발</p>
    <p>회원가입 및 프로필 수정 validation 기능 개발</p>
    <ul class="describeLibrarys">
      <li class="library"></li>
      <li class="library"></li>
      <li class="library"></li>
      <li class="library"></li>
    </ul>
  </article>
</template>
<style scoped>
.describeContainer {
  display: flex;
  flex-direction: column;
}
.describeIcon {
  width: 43px;
  height: 43px;
  background-color: pink;
  margin-bottom: 50px;
}
.describeTitle {
  font-size: 24px;
  font-weight: bold;
  color: #333;
  margin-bottom: 50px;
  cursor: pointer;
}
.describeContainer > p {
  color: #827d7d;
  margin-bottom: 10px;
  font-weight: 500;
}
.describeLibrarys {
  width: fit-content;
  height: fit-content;
  display: flex;
  gap: 20px;
  list-style: none;
  padding-left: 0;
}
.library {
  cursor: pointer;
  margin-top: 40px;
  text-decoration: none;
  width: 30px;
  height: 30px;
  border-radius: 5px;
  background: lightblue;
}
</style>
