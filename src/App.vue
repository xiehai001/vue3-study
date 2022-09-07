<script setup>
import { reactive, ref, shallowRef, defineAsyncComponent } from 'vue'
import { useIntersectionObserver } from '@vueuse/core'
import Child1 from './components/Child1.vue'
import Child2 from './components/Child2.vue'

const Child3 = defineAsyncComponent(() =>
import('./components/Child3.vue')
)


const target = ref(null)
const targetIsVisible = ref(false)

const { stop } = useIntersectionObserver(
target,
([{ isIntersecting }]) => {
if (isIntersecting) {
targetIsVisible.value = isIntersecting
}
},
)

</script>

<template>
  <div>
    <Child1></Child1>
    <Child2></Child2>
    <div ref="target">
      <Child3 v-if="targetIsVisible"></Child3>
    </div>
  </div>
</template>

<style scoped>
</style>  
