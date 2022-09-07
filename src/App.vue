<script setup>
import List from './components/List.vue'
import { reactive, ref } from 'vue'
let childMsg = ref('');
const childFn = (data) => {
childMsg.value = data
}
</script>

<template>
  <div>
    来自子组件的数据=》 {{childMsg}}
    <List @childFn="childFn"></List>
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
