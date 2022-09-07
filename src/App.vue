<script setup>
import { reactive, ref, shallowRef } from 'vue'
import Tab1 from './components/Tab1.vue'
import Tab3 from './components/Tab3.vue'
import Tab2 from './components/Tab2.vue'
const componetName = ref(Tab1)
const tablist = reactive([
{ name: 'tab1', component: shallowRef(Tab1) },
{ name: 'tab2', component: shallowRef(Tab2) },
{ name: 'tab3', component: shallowRef(Tab3) },
]);
const changeTab = (item) => {
componetName.value = item.component
}


</script>

<template>
  <div>
    <ul>
      <li v-for="(item,index) in tablist" :key="index" @click="changeTab(item)">{{item.name}}</li>
    </ul>
    <keep-alive>
      <component :is="componetName"></component>
    </keep-alive>
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
