<template>
  <!-- Button trigger modal -->
  <button
    type="button"
    class="btn btn-primary"
    data-bs-toggle="modal"
    data-bs-target="#staticBackdrop"
  >
    커피 후원하기
  </button>

  <!-- Modal -->
  <div
    class="modal fade"
    id="staticBackdrop"
    data-bs-backdrop="static"
    data-bs-keyboard="false"
    tabindex="-1"
    aria-labelledby="staticBackdropLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="staticBackdropLabel">
            ☕ 한 잔의 커피 후원하기
          </h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body">
          <div>
            <button @click="selectQR('toss')">토스</button>
            <button @click="selectQR('kakao')">카카오페이</button>
          </div>
          <div>
            <img v-if="QR == 'toss'" src="@/assets/토스.png" />
            <img v-if="QR == 'kakao'" src="@/assets/카카오페이.png" />
          </div>
        </div>
        <div class="modal-footer">
          <input class="cheer flex-fill" v-model="message" type="text" placeholder="응원의 메세지를 적어주세요"/>
          <button v-if="QR == 'toss'" @click="sendMessage()" type="button" class="btn btn-primary" data-bs-dismiss="modal">응원 보내기</button>
          <button v-if="QR == 'kakao'" @click="sendMessage()" type="button" class="btn btn-warning" style="color: white;" data-bs-dismiss="modal">응원 보내기</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import {ref} from "vue";

const QR = ref('toss');
const message = ref(null);

function selectQR(value) {
  QR.value = value;
}

function sendMessage() {
  console.log(message.value);
}
</script>

<style scoped>
.modal-footer {
  width: 100%;
}
.cheer {
  border: none;
  outline: none;
}
</style>
