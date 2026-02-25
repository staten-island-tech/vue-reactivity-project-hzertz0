<template>
    <head>    
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap" rel="stylesheet"/>
    </head>
    <div>
        <h1>Potion Brewer</h1>
        <div class ="cauldron">
            <h1>Cauldron</h1>
            <img src="/cauldron.png">
        </div>
        <div class = "container">
            <!--<ingredients v-for="item in list" :key="item.name":item="item"/>-->
        </div>
    </div>
</template>

<script setup>

import ingredients from '@/components/ingredients.vue'
const list = [
    {name: "Bat Wings",description: "A pair of wings from a bat",image: "/batwings.png"},
    {name: "Dragon Scales",description: "Scales harvested from a magical dragon",image: "./dragonscale.png"},
    {name: "Jellybeans",description: "Some jellybeans from a random gas station",image: "./jellybean.png"},
]

</script>

<style scoped>
*{
    font-family: "inter";
    text-align: center ;
}

.cauldron {
    width: 50%;
    height: 750px;
    color: white;
    background-color: black;
}

img {
    max-height: 500px;
    width: auto
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