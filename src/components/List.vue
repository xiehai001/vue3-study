<template>
    <div>
        <button @click="send">发送数据</button>
    </div>
</template>

<script setup>
import { ref, defineEmits } from "vue";
const emit = defineEmits(['childFn'])
const childMsg = ref('子组件数据')
const send = () => {
emit('childFn', childMsg)
}

</script>

<style lang="scss" scoped>
</style>