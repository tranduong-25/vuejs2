<template>
  <div>
    <input type="text" :disabled="isDisable" placeholder="Không cho phép nhập" />
    <input type="text" :disabled="!isDisable" placeholder="Cho phép nhập" />
    <p>isDisable={{ isDisable }}</p>
    <p>isDisable={{ !isDisable }}</p>

    <!-- Button to toggle isDisable -->
    <button @click="toggleDisable">Toggle Disable</button>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'Exercice03',
  setup() {
    const isDisable = ref(true);
    const toggleDisable = () => {
      isDisable.value = !isDisable.value;
    };

    return {
      isDisable,
      toggleDisable,
    };
  },
};
</script>

<style scoped>
input {
  margin: 10px;
}
</style>
