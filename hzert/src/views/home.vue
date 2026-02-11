<template>
    <div>
        <ingredients v-for="item in list" :key="item.name":item="item"/>
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

</style>