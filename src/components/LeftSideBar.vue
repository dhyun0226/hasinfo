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
  {emoji: "đ", name: "ě ě˛´", value: "total" },
  {emoji: "đĄ", name: "ě¤ę° íëŤíź", value: "1" },
  {emoji: "đˇ", name: "ëźě´íě¤íěź", value: "2" },
  {emoji: "đ°", name: "ę¸ěľ", value: "2" },
  {emoji: "đŤ", name: "ěě", value: "2" },
  {emoji: "đ", name: "ëŻ¸ëě´", value: "2" },
  {emoji: "âď¸", name: "ęľěĄ", value: "2" },
  {emoji: "đ˛", name: "ěě°ěą", value: "2" },
  {emoji: "đ", name: "ë¸ëĄě˛´ě¸", value: "2" },
  {emoji: "đť", name: "ë¸ě˝ë", value: "2" },
  {emoji: "đ¤", name: "ě¸ęłľě§ëĽ", value: "2" },
  {emoji: "đ", name: "ěť¤ëŽ¤ëí°", value: "2" },
  {emoji: "đ", name: "ëśěí´", value: "2" },
  {emoji: "đ¨", name: "ëěě¸", value: "2" },
  {emoji: "đ§âđť", name: "ę°ë°í´", value: "2" },
  {emoji: "đŽ", name: "ë§ěźíí´", value: "2" },
  {emoji: "đŽ", name: "ę˛ě", value: "2" },
  {emoji: "đł", name: "ě´ěť¤ë¨¸ě¤", value: "2" },
  {emoji: "đ", name: "íŹě¤ěźě´", value: "2" },
  {emoji: "đ§Ź", name: "ë°ě´ě¤", value: "2" },
  {emoji: "đ", name: "ëŠíë˛ě¤", value: "2" },
  {emoji: "đ¸", name: "ě¸ěźěŚ", value: "2" },
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
