<template>
  <Navbar />
  <div class="container-xxl">
    <div class="row">
      <LeftSideBar class="col-3" />
      <router-view class="col-6" />
      <RightSideBar class="col-3" />
    </div>
  </div>
</template>

<script setup>
import Navbar from "@/components/Navbar.vue";
import LeftSideBar from "@/components/LeftSideBar.vue";
import RightSideBar from "@/components/RightSideBar.vue";

</script>

<style>
#app {
  font-family: -apple-system, BlinkMacSystemFont, "Apple SD Gothic Neo", Pretendard, Roboto, "Noto Sans KR", "Segoe UI", "Malgun Gothic", "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  background-color: rgb(245, 245, 247);
}
</style>
