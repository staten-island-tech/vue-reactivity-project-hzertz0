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
    <div class="panel" ref="panel">
      <ingredients @click="addToPotion(item)" v-for="item in list" :key="item.name" :item="item">
        <button>Add Ingredient</button>
      </ingredients>
    </div>
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

const panel = ref()
function showIngredients() {
  panel.value.classList.toggle('open')
}

const cauldron = []
function addToPotion(item){
  cauldron.push(item)
  console.log(cauldron)
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

button {
  background-color: rgb(255, 255, 255);
  border: none;
  color: rgb(0, 0, 0);
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 20px;
  margin: 4px 2px;
  cursor: pointer;
  border-radius: 12px;
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
  position: fixed;
  top: 0;
  right: 0;
  width: 0;
  height: 100%;
  background-color: rgb(68, 196, 106);
  transition: width 0.4s ease;
  overflow: scroll;
}

.panel.open {
  width: 250px;
  padding: 20px;
}
</style>
