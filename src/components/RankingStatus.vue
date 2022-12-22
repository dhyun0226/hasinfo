<template>
  <div class="container">
    <div class="title" v-if="data.title === 'study'">
      🔥 실시간 스터디 순위
    </div>
    <div class="title" v-else-if="data.title === 'club'">
      🔥 실시간 동호회 순위
    </div>
    <div class="contents">
      <div v-for="content in data.contents" :key="content.rank">
        <div class="content" @click="moveContentPage(content)">
          <div class="rank">{{ content.rank }}</div>
          <div class="img">{{ content.img }}</div>
          <div class="name-tag">
            <div class="name">{{ content.name }}</div>
            <div class="tag">{{ content.tag }}</div>
          </div>
          <div class="new" v-if="content.new">new</div>
        </div>
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

const { data } = toRefs(props); //html template에서 props.data.title이라고 사용하지 않고, data.title이라고 사용하기 위해

function moveContentPage(content) {
  console.log(data.value.title);
  console.log(content.name);  //나중에 name 사이에 있는 Space를 -로 처리할 것(근데 이걸 백엔드에서 처리할 지, 프론트에서 처리할 지는 고민)
  console.log(content);
}


</script>

<style scoped>
.container {
  min-width: 310px;
}

.contents {
  background-color: white;
  border-radius: 20px;
}

.contents {
  background-color: white;
  padding: 10px 10px;
  cursor: pointer;
}

.content {
  display: flex;
  align-items: center;
  margin: 5px;
  color: rgb(142, 142, 142);
  gap: 8px;
}

.img {
  min-width: 40px;
  width: 40px;
  height: 40px;
  border-radius: 14px;
  background-color: red;
  background-position: center center;
  background-size: cover;
}

.name {
  font-size: 14px;
}

.tag {
  font-size: 12px;
}

.new {
  color: orange;
}
</style>
