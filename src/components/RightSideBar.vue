<template>
  <div class="rightSideBar">
    <div>개발자에게</div>
    <CoffeeModal></CoffeeModal>
    <button class="btn btn-success">버그 제보하기</button>
    <button class="btn btn-danger">기능 요청하기</button>
    <button class="btn btn-warning">기능 요청하기</button>
    <div class="status">
      <RankingStatus :data="club"/>
      <RankingStatus :data="study"/>
    </div>
  </div>
</template>

<script setup>
import RankingStatus from "./RankingStatus.vue";
import CoffeeModal from "@/components/CoffeeModal.vue";
import { ref, reactive } from "vue";

const club = reactive({
  title: "club",
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

const study = reactive({
  title: "study",
  contents: [
    { rank: 1, img: 1, name: "Vue를 사랑하는 모임" },
    { rank: 2, img: 2, name: "DB를 사랑하는 모임" },
    { rank: 3, img: 3, name: "JS를 사랑하는 모임" },
    { rank: 4, img: 4, name: "스프링을 사랑하는 모임", new: true},
    { rank: 5, img: 5, name: "자전거를 사랑하는 모임" },
  ],
});
</script>

<style scoped>
.status {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  position: sticky;
  top: 5rem;
  margin-top: 20px;
}
</style>
