<script setup>
import {useRoute} from "vue-router";
import cars from "../data/cars.json";

const route = useRoute();
const car = cars.find(c => c.id === parseInt(route.params.id));

</script>
<template>
    <div v-if="car">
        <h3>Contact Info:</h3>
        <p>{{car.contact.dealer}}</p>
        <p>{{car.contact.number}}</p>
    </div>
</template>

<style scoped>
h3 {
    margin: 10px 0 0;
    font-weight: 600;
    color:blueviolet;
}
</style>