<template>
    <head>    
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap" rel="stylesheet"/>
    </head>
    <div>
        <h1>Potion Brewer</h1>
        <div class = "container">
            <ingredients v-for="item in list" :key="item.name":item="item"/>
        </div>
    </div>
</template>

<script setup>
import ingredients from '@/components/ingredients.vue'
const list = [
    {name: "Bat Wings",effect: "die",image: "/"},
    {name: "Dragon Scales",effect: "big",image: "/"},
    {name: "Fairy Dust",effect: "small",image: "/"},
    {name: "Jellybean",effect: "boom",image: "/"},
    {name: "Bear Claw",effect: "bang",image: "/"}
]

</script>

<style scoped>
*{
    font-family: "inter";
    text-align: center ;
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