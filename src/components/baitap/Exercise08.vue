<template>
  <div>
    <p>Company: {{ info.company }}</p>
    <p>Age: {{ info.age }}</p>
    <button @click="updateInfo">Change data</button>
  </div>
</template>

<script setup>
import { reactive } from 'vue';

const info = reactive({
  company: 'Rikkei Academy',
  age: 2
});
const updateInfo = () => {
  info.company = 'Rikkei Education';
  info.age = 1;
};
</script>

<style scoped>
</style>
