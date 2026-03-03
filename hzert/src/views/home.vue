<template>
  <div class="ingredients">
    <h1>Ingredients</h1>
    <div class="addedingredients">
      <div class="adds"></div>
      <div class="adds"></div>
      <div class="adds"></div>
      <div class="adds"></div>
      <div class="adds"></div>
      <div class="adds"></div>
    </div>
    <button @click="showIngredients">View Ingredients</button>
    <div class="panel"></div>
    <!-- <ingredients v-for="item in list" :key="item.name" :item="item" @add="addToPotion" />-->
  </div>
</template>

<script setup>
import ingredients from '@/components/ingredients.vue'
import { ref } from 'vue'
const list = ref([
  { name: 'Bat Wings', description: 'A pair of wings from a bat', image: '/batwings.png' },
  {
    name: 'Dragon Scales',
    description: 'Scales harvested from a magical dragon',
    image: './dragonscale.png',
  },
  {
    name: 'Jellybeans',
    description: 'Some jellybeans from a random gas station',
    image: './jellybean.png',
  },
])

function showIngredients(){
  panel.classList.toggle("open");
}

</script>

<style>
* {
  font-family: 'inter';
  text-align: center;
}

body {
  margin: 0;
  font-family: 'Inter', sans-serif;

  background-image: url('/background.png');
  background-attachment: fixed;
  background-size: cover;
}

.ingredients {
  color: white;
  position: absolute;
  left: 58.25%;
  top: 22.5%;
  width: 25%;
  height: 50%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.adds {
  color: black;
  background-color: rgb(117, 200, 255);
  width: 200px;
  height: 75px;
  border: 1px solid rgb(255, 255, 255);
  border-radius: 10px;
  margin: 2.5px;
}

.addedingredients {
  margin: 25px;
  margin-left: 25px;
  margin-right: 25px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.panel {
  width: 0;
}

.panel.open {
  width: 300px;
  padding: 20px;
}

</style>
