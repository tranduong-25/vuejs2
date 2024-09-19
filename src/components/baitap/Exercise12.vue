<template>
  <div>
    <input type="number" v-model="inputValue" placeholder="Enter amount" />
    <button @click="addToCart">Add to cart</button>
    
    <p>Tổng tiền trong giỏ hàng: {{ totalAmount }}</p>
    <p>Input: {{ inputValue }}</p>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';
const totalAmount = ref(0);
const inputValue = ref(0);

const addToCart = () => {
  totalAmount.value += Number(inputValue.value); 
  inputValue.value = 0; 
};

const displayedTotalAmount = computed(() => totalAmount.value);
</script>

<style scoped>
</style>
