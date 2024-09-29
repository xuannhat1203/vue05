<template>
  <div>
    <h4>Gender: {{ gender }}</h4>
    <button @click="handleClick">Random Gender</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const data = ["male", "female"];
const getRandom = () => {
  const randomIndex = Math.floor(Math.random() * data.length);
  return data[randomIndex];
};
const gender = ref("male")
const handleClick = () => {
  gender.value = getRandom();
};

</script>

<style></style>
