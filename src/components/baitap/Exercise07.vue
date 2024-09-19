
<template>
  <div>
    <p>Count: {{ count }}</p>
    <button @click="count++">Click me</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);
</script>

<style scoped>
</style>
