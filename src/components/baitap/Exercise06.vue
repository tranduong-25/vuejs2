<template>
  <div>
    <button @click="handleClick('Rikkei Academy')">Get param</button>
  </div>
</template>

<script>
export default {
  name: 'Exercice06',
  setup() {
    const handleClick = (param) => {
      console.log(param); 
    };

    return {
      handleClick,
    };
  },
};
</script>

<style scoped>
button {
  margin: 10px;
  padding: 10px 20px;
  font-size: 16px;
}
</style>
