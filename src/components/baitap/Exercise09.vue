<!-- Exercise03.vue -->
<template>
  <div>
    <p>Khi Width= {{ width }}</p>
    <p>Height= {{ height }}</p>
    <p>Acreage: {{ area }}</p>
    <button @click="increaseWidth">Change data</button>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const width = ref(10);
const height = ref(20);
const area = computed(() => width.value * height.value);
const increaseWidth = () => {
  width.value += 10;
};
</script>

<style scoped>
</style>
