<template>
  <div>
    <h2>{{ item.name }}</h2>
    <img :src="item.image" />
    <p>{{ item.description }}</p>
    <button @click="addToCart(item)">Add Ingredient</button>
  </div>
</template>

<script setup>
defineProps({
  item: {
    type: Object,
    required: true,
  },
})
</script>

<style scoped>
* {
  font-family: 'inter';
}

img {
  max-width: 150px;
  height: auto;
}

div {
  color: rgb(0, 0, 0);
  width: 150px;
  height: auto;
  font-size: 20px;
  margin: 25px auto;
  border-radius: 10px;
  padding: 10px;
  text-align: center;
  justify-content: center;
  box-shadow:
    0 4px 8px 0 rgba(0, 0, 0, 0.2),
    0 6px 20px 0 rgba(0, 0, 0, 0.19);
  background-color: rgb(63, 161, 63);
}

div:hover {
  transform: scale(1.05);
  transition: transform 0.3s ease;
}
button {
  background-color: green;
  border: none;
  color: rgb(255, 255, 255);
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 20px;
  margin: 4px 2px;
  cursor: pointer;
  border-radius: 12px;
}
</style>
