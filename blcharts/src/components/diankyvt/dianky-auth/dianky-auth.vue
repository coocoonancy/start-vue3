<script setup>
import { defineProps, defineEmits } from 'vue'
const props = defineProps({
  pid: String,
  did: String,
  mode: String
})
const emit = defineEmits(['back'])
function emitBack() {
  emit('back')
}
</script>
<template>
  <div class="dianky-auth">
    <div class="btnBox">{{ mode }}</div>
    <div class="btnBox">{{ pid }}</div>
    <div class="btnBox" @click="emitBack">返回</div>
  </div>
</template>

<style scoped>
.dianky-auth {
  background-color: #ffffff;
}
.btnBox {
  width: 100%;
  height: 50px;
  position: relative;
}
</style>
