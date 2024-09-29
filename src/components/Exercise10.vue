<template>
    <div>
      <button @click="handleClick">Random number</button>
      <h4>{{ randomNumbers }}</h4>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';

  const randomNumbers = ref([]);
  
  const getRandomNumbers = () => {
    const randomArray = [];
    for (let i = 0; i < 10; i++) { 
      const randomNum = Math.floor(Math.random() * 100); 
      randomArray.push(randomNum);
    }
    return randomArray;
  };
  
  
  const handleClick = () => {
    randomNumbers.value = getRandomNumbers();
  };
  </script>
  
  <style>
  </style>
  