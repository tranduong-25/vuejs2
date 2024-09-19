<!-- Exercise04.vue -->
<template>
  <div>
    <input v-model="inputValue" placeholder="Enter something" />
  </div>
</template>

<script setup>
import { ref, watch } from 'vue';

// Tạo một ref để lưu trữ giá trị nhập từ input
const inputValue = ref('');

// Sử dụng watch để theo dõi sự thay đổi của inputValue
watch(inputValue, (newValue, oldValue) => {
  console.log(`Input changed from "${oldValue}" to "${newValue}"`);
});
</script>

<style scoped>
/* Add styles here if cần */
</style>
