<script setup>
import { reactive } from 'vue'
// 无法响应
// const obj = {
// a: 1,
// b: 2
// }
// const add = () => {
// obj['c'] = 1
// }

// 响应式

const obj = reactive({
a: 1,
b: 2
})
const add = () => {
obj['c'] = 1
}

</script>

<template>
  <div>
    {{obj}}
    <button @click="add">添加</button>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
