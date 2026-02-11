<template>
    <head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap" rel="stylesheet"/>
    </head>
    <div>
        <h2>{{ item.name }}</h2>
        <h3>{{ item.effect}}</h3>
    </div>
</template>

<script setup>
defineProps({
    item:{
        type:Object,
        required: true,
    }
})
</script>

<style scoped>
*{
    font-family: "inter";
}

div {
    width: 300px;
    height: auto;
    font-size: 20px;
    margin: 25px auto;
    border-radius: 10px;
    padding: 10px;
    text-align: center ;
    justify-content: center;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

div:hover {
    transform: scale(1.05);
    transition: transform 0.3s ease;
}
</style>