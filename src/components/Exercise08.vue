<template>
    <div>
        <button @click="handleClick">Tăng dần</button>
        <button @click="handleClickDescending">Giảm dần</button>
        <ul>
            <li v-for="num in data" :key="num">{{ num }}</li>
        </ul>
    </div>
</template>

<script setup>
import { ref } from 'vue';
const data = ref([1, 4, 2, 3, 5, 8, 7, 6]);
const handleClick = () => {
    data.value.sort((a, b) => a - b);
};
const handleClickDescending = () => {
    data.value.sort((a, b) => b - a);
};
</script>

<style>
</style>
