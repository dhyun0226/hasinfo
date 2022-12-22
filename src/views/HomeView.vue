<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
      <Open />

    <!-- 메인 리스트에 뜨는 화면은 v-for와 v-if를 이용해서 개설 컴포넌트, 활동내역 컴포넌트 등을 반복해서 보여줌(최신순) -->
    <!-- <div class="container text-center">
      <div class="row">
        <div class="col"><i class="bi bi-trash2"></i>Column</div>
        <div class="col">Column</div>
        <div class="col">Column</div>
      </div>
    </div> -->
  </div>
</template>

<script setup>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Open from "@/components/main/Open.vue";
import { ref, reactive } from "vue";

const club = reactive({
  name: "🔥 실시간 동호회 순위",
  contents: [
    {
      rank: 1,
      img: 1,
      name: "자전거를 사랑하는 모임",
      tag: "서울 1등 자전거 모임!",
      new: true,
    },
    { rank: 2, img: 2, name: "자전거를 사랑하는 모임" },
    { rank: 3, img: 3, name: "자전거를 사랑하는 모임" },
    { rank: 4, img: 4, name: "자전거를 사랑하는 모임" },
    { rank: 5, img: 5, name: "자전거를 사랑하는 모임" },
  ],
});
</script>
