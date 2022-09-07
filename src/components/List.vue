<template>
    <div>
        {{num}}
        <button @click="send">改变数据</button>
    </div>
</template>

<script setup>
import { ref } from "vue";

const emit = defineEmits(['update:num'])
const props = defineProps({
num: {
type: Number,
default: 100
}
})
const send = () => {
emit('update:num', 500)
}
</script>

<style lang="scss" scoped>
</style>