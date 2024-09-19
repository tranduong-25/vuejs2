<!-- ShoppingCart.vue -->
<template>
  <div>
    <h2>Giỏ hàng</h2>
    <ul>
      <li v-for="(product, index) in products" :key="index">
        <span>{{ product.name }} - Số lượng: {{ product.quantity }}</span>
        <button @click="increaseQuantity(index)">Tăng số lượng</button>
      </li>
    </ul>
    
    <h3>Tổng số lượng sản phẩm: {{ totalQuantity }}</h3>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';
const products = ref([
  { name: 'Mèn mén loại 1', quantity: 1 },
  { name: 'Mèn mén loại 2', quantity: 2 },
  { name: 'Mèn mén loại 3', quantity: 3 }
]);

const increaseQuantity = (index) => {
  products.value[index].quantity += 1;
};
const totalQuantity = computed(() => {
  return products.value.reduce((total, product) => total + product.quantity, 0);
});
</script>

<style >
</style>
