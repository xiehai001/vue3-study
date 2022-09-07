<template>
    <div>
        子组件
        ==>{{msg}}
    </div>
</template>

<script setup>
defineProps({
msg: {
type: String,
default: ''
}
})
</script>

<style lang="scss" scoped>
</style>