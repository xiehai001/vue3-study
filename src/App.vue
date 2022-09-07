<script setup>
import { reactive, ref } from 'vue'
import List from './components/List.vue'
let msg = ref('父组件的数据')
</script>

<template>
  <div>
    <List :msg="msg"></List>
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
