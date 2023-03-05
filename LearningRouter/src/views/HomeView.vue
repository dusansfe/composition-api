
<script setup>
import cars from "../data/cars.json";
import { RouterLink } from "vue-router";
</script>
<template>
    <div class="spacing">
        <h1>Home view</h1>
        <div class="cars">
            <RouterLink v-for="car in cars" :key="car.id" :to="`/cars/${car.id}`">
                {{car.name}}
            </RouterLink>
        </div>
    </div>
</template>

<style scoped>
.cars {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
.cars a {
    text-decoration: none;
    color: black;
    width: 100%;
    max-width: 150px;
    box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.208);
    margin: 10px;
    padding: 5px 10px;
    text-align: center;
}
</style>