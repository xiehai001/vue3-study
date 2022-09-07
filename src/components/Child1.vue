<template>
    <div>
        <header>头部
            <slot name="header"></slot>
        </header>
        <section>内容
            <slot name="content"></slot>

            <ul>
                <li v-for="item in data" :key="item.name">
                    <slot :data="item"></slot>
                </li>
            </ul>
        </section>
        <footer>底部
            <slot name="footer"></slot>
        </footer>
    </div>
</template>

<script setup>
import { ref } from "vue";

const data = ref([
{ name: '花裤1', age: 20 },
{ name: '花裤2', age: 21 },
{ name: '花裤3', age: 24 },
{ name: '花裤4', age: 25 },
])
</script>

<style lang="scss" scoped>
</style>