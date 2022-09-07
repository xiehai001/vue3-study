<script setup>
import { reactive, ref } from 'vue'
import Child1 from './components/Child1.vue';
import Child2 from './components/Child2.vue';

</script>

<template>
  <div>
    <Child1></Child1>
    <Child2></Child2>
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
