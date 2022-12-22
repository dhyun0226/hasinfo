<template>
  <div class="home">
    <TitleBox class="titleBox" :data="props"/>
    <OpenBox class="openBox"/>
  </div>
</template>

<script setup>
// @ is an alias to /src
import { ref, reactive } from "vue";
import OpenBox from "./parts/OpenBox.vue";
import TitleBox from "./parts/TitleBox.vue";

const props = reactive({
  title: "club",
  contents: {
    name: "이동현",
    position: "사원",
    department: "CRM서비스개발팀",
    time: "약 5시간 전",
  }
});

</script>

<style scoped>

.titleBox {
    margin-bottom: 10px;
}

.openBox {
    padding: 0px 30px;
}
</style>
