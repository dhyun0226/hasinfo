<template>
  <div class="container">
    <div class="LeftSideBar">
      <div class="title d-flex" @click="toggleTopic($event)">
        <i class="bi bi-caret-right" :class="{ clicked, unclicked }" ></i>
        <span>Topics</span>
      </div>
      <div class="content">
        <ul :class="{ clicked, unclicked }">
          <li v-for="(topic, index) in topics" :key="index" @click="changeTopic(topic, $event)">
            {{ topic.emoji }}
            {{ topic.name }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive } from "vue";

const clicked = ref(false);
const unclicked = ref(true);

const topics = ref([
  {emoji: "🌕", name: "전체", value: "total" },
  {emoji: "📡", name: "중개 플랫폼", value: "1" },
  {emoji: "📷", name: "라이프스타일", value: "2" },
  {emoji: "💰", name: "금융", value: "2" },
  {emoji: "👫", name: "소셜", value: "2" },
  {emoji: "🎙", name: "미디어", value: "2" },
  {emoji: "✏️", name: "교육", value: "2" },
  {emoji: "🚲", name: "생산성", value: "2" },
  {emoji: "🔗", name: "블록체인", value: "2" },
  {emoji: "💻", name: "노코드", value: "2" },
  {emoji: "🤖", name: "인공지능", value: "2" },
  {emoji: "🏘", name: "커뮤니티", value: "2" },
  {emoji: "📊", name: "분석툴", value: "2" },
  {emoji: "🎨", name: "디자인", value: "2" },
  {emoji: "🧑‍💻", name: "개발툴", value: "2" },
  {emoji: "🔮", name: "마케팅툴", value: "2" },
  {emoji: "🎮", name: "게임", value: "2" },
  {emoji: "💳", name: "이커머스", value: "2" },
  {emoji: "🏃", name: "헬스케어", value: "2" },
  {emoji: "🧬", name: "바이오", value: "2" },
  {emoji: "👓", name: "메타버스", value: "2" },
  {emoji: "💸", name: "세일즈", value: "2" },
]);

function toggleTopic(event) {
 console.log(event);
 this.clicked = !this.clicked
 this.unclicked = !this.unclicked
}

function changeTopic(topic, event) {
  alert(topic.value);
}

</script>

<style scoped>

.container {
  padding-left: 50px;
}

.title {
  margin-bottom: 0.5rem;
}

ul {
  list-style: none;
  overflow-y: scroll;
  height: calc(100vh - 150px);
  margin-right: 50px;
}

li {
  margin-right: 5px;
  margin-bottom: 5px;
}

li:hover {
  color: orange;
  cursor: pointer;
  border-color: orange;
  background-color: white;
  border-radius: 10%;
}

.LeftSideBar {
  position: sticky;
  top: 5rem;
  margin-top: 10px;
}

i.clicked {
  transform: rotate(90deg);
  transition: transform 0.5s ease-in-out;
}

i.unclicked {
  transform: rotate(0deg);
  transition: transform 0.5s ease-in-out;
}

ul.clicked {
  transform: rotate(90deg);
  transition: transform 0.5s ease-in-out;
}

ul.unclicked {
  transform: rotate(0deg);
  transition: transform 0.5s ease-in-out;
}

</style>
