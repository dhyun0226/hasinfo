<template>
<div>
  <div class="container">
    <div class="img"></div>
    <div class="content">
      <div class="title">
        <div class="name">미라클나잇</div>
        <div class="like-count"><i class="bi bi-hand-thumbs-up"></i> 20</div>
      </div>
      <div class="description">
        고농축 슬립샷으로 세계 최고의 수면을 경험하다
      </div>
      <div class="label">
        <div class="tag">🚗 헬스케어</div>
        <div class="tag">🎭 인공지능</div>
        <div class="tag">🎆 라이프스타일</div>
        <div class="tag comment-count">💬 5</div>
        <div class="tag view-count">👀 120</div>
      </div>
    </div>
  </div>
</div>
</template>

<script setup></script>

<style scoped>
.container {
  display: flex;
  background-color: white;
  border-radius: 16px;
  padding: 16px;
  transition: box-shadow 0.3s;
}

.img {
  display: block;
  min-width: 80px;
  min-height: 80px;
  max-height: 80px;
  background-color: tomato;
  border-radius: 14px;
  box-shadow: rgb(0 0 0 / 10%) 0px 0px 4px;
}

.content {
  display: flex;
  flex-direction: column;
  color: rgb(142, 142, 142);
  justify-content: space-around;
  margin-left: 16px;
  width: 100%;
}

.title {
  display: flex;
  justify-content: space-between;
}

.name {
  color: black;
  font-size: 16px;
  font-weight: bold;
}

.like-count {
  font-size: 14px;
  align-self: center;
  border: 1px solid rgb(142, 142, 142);
  border-radius: 10px;
  padding: 1px 6px;
}

.description {
  font-size: 14px;
}

.label {
  display: flex;
  gap: 4px;
  font-size: 12px;
}

.tag {
  background-color: rgb(236, 236, 238);
  color: rgb(112, 112, 112);
  border-radius: 16px;
  padding: 2px 8px;
}

.club {
  color: orange;
}

.study {
  color: rgb(109, 85, 255);
}

.container:hover {
  box-shadow: 0 0 11px rgba(33, 33, 33, 0.2);
}

.like-count:hover {
  color: orange;
  cursor: pointer;
  border-color: orange;
}
</style>
