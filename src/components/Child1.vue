<template>
    <div>
        child1
        <button @click="send">传送数据</button>
        <hr />
    </div>
</template>

<script setup>
import bus from '../bus'
import { ref } from 'vue'
const data1 = ref('child1 的数据')
const send = () => {
bus.emit('sendChild1', data1)
}
</script>

<style lang="scss" scoped>
</style>