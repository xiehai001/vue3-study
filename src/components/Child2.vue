<template>
    <div>
        Child2
        {{child1Data}}
    </div>
</template>

<script setup>
import bus from '../bus'
import { ref } from 'vue'
let child1Data = ref('')
bus.on('sendChild1', (data) => {
console.log(data)
child1Data.value = data
})
</script>

<style lang="scss" scoped>
</style>