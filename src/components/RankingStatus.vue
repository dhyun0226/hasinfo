<template>
  <div class="container">
    <div class="title" v-if="data.title === 'study'">
      ๐ฅ ์ค์๊ฐ ์คํฐ๋ ์์
    </div>
    <div class="title" v-else-if="data.title === 'club'">
      ๐ฅ ์ค์๊ฐ ๋ํธํ ์์
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

const { data } = toRefs(props); //html template์์ props.data.title์ด๋ผ๊ณ  ์ฌ์ฉํ์ง ์๊ณ , data.title์ด๋ผ๊ณ  ์ฌ์ฉํ๊ธฐ ์ํด

function moveContentPage(content) {
  console.log(data.value.title);
  console.log(content.name);  //๋์ค์ name ์ฌ์ด์ ์๋ Space๋ฅผ -๋ก ์ฒ๋ฆฌํ  ๊ฒ(๊ทผ๋ฐ ์ด๊ฑธ ๋ฐฑ์๋์์ ์ฒ๋ฆฌํ  ์ง, ํ๋ก ํธ์์ ์ฒ๋ฆฌํ  ์ง๋ ๊ณ ๋ฏผ)
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
