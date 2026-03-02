<template>
  <head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap"
      rel="stylesheet"
    />
  </head>
      <div class ="ingredients">
        <h1>Ingredients</h1>
        <div class="container">
          <ingredients v-for="item in list" :key="item.name" :item="item"/>
        </div>
    </div>
</template>

<script setup>
import ingredients from '@/components/ingredients.vue'
const list = [
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
]

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

.container {
  margin: 25px;
  margin-left: 25px;
  margin-right: 25px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
