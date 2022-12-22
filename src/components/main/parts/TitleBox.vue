<template>
  <div class="container">
    <div class="img"></div>
    <div class="content">
      <div class="title">
        <div class="name">{{ data.contents.name }}</div>
        <span class="name-badge"><i class="bi bi-check-circle-fill"></i></span>
        <div class="description">
          <span>님이 </span>
          <span v-if="data.title === 'club'" :class="data.title">동아리</span>
          <span v-if="data.title === 'study'" :class="data.title">스터디</span>
          <!-- 동아리, 스터디 -->
          <!-- <span class="club">{{ "동아리" }}</span> -->
          <!-- <span class="study">{{ "스터디" }}</span> -->
          <span>를 개설하였습니다.</span>
        </div>
        <div class="divider">•</div>
        <div class="follow-button">팔로우</div>
      </div>
      <div class="label">
        <div class="user-position">{{ data.contents.position }}</div>
        <!-- 사원 -->
        <div class="user-department">@{{ data.contents.department }}</div>
        <!-- CRM서비스개발팀 -->
        <div class="divider">•</div>
        <div class="post-time">{{ data.contents.time }}</div>
        <!-- 약 5시간 전 -->
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, toRefs } from "vue";
const props = defineProps({
  data: {
    title: String,
    contents: Array,
  },
});

const { data } = toRefs(props);

console.log(data);
console.log(data.value);
</script>

<style scoped>
.container {
  display: flex;
  padding: 0px;
}

.img {
  min-width: 40px;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  margin-right: 8px;
  background-color: red;
  background-position: center center;
  background-size: cover;
}

.content {
  display: flex;
  flex-direction: column;
  color: rgb(142, 142, 142);
}

.title {
  display: flex;
  gap: 4px;
}

.name {
  font-weight: bold;
  color: black;
}

.name-badge {
  color: rgb(0, 133, 255);
}

.label {
  display: flex;
  font-size: 0.75rem;
  gap: 4px;
}

.club {
  color: orange;
}

.study {
  color: rgb(109, 85, 255);
}

.follow-button {
  color: rgb(0, 133, 255);
  font-size: 14px;
  align-self: center;
}

.name:hover,
.follow-button:hover {
  color: orange;
  cursor: pointer;
}
</style>
