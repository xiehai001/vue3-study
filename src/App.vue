<script setup>
import List from './components/List.vue'
import { reactive, ref } from 'vue'
let num = ref(100)

</script>

<template>
  <div>
    <List v-model:num="num"></List>
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
