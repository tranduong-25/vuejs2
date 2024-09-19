<template>
  <div>
    <div 
      :class="{'active': isActive}" 
      :style="{ backgroundColor: backgroundColor }" 
      class="block"
    >
      Block
    </div>
    <p>isActive={{ isActive }}</p>
    <button @click="toggleActive">Toggle Active</button>
    <select v-model="backgroundColor">
      <option value="blue">Blue</option>
      <option value="red">Red</option>
      <option value="green">Green</option>
    </select>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'Exercice04',
  setup() {
    // Declare isActive and backgroundColor variables
    const isActive = ref(true);
    const backgroundColor = ref('blue');

    // Function to toggle isActive
    const toggleActive = () => {
      isActive.value = !isActive.value;
    };

    return {
      isActive,
      backgroundColor,
      toggleActive,
    };
  },
};
</script>

<style scoped>
.block {
  width: 200px;
  height: 100px;
  margin: 10px;
  color: black;
  text-align: center;
  line-height: 100px;
}

.active {
  color: #fff;
}
</style>
