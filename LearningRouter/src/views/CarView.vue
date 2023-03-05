<script setup>
    import { useRoute, useRouter, RouterView } from 'vue-router';
    import cars from "../data/cars.json";

    const route = useRoute();
    const router = useRouter();

    const carID = parseInt(route.params.id);

    const car = cars.find(c => c.id === parseInt(route.params.id));

    const showContact = () => {
        if(carID === 4) return;

        return router.push(`/cars/${carID}/contact`);
    }

</script>
<template>
    <div v-if="car">
        <h1>Car View</h1>
        <h2>{{car.name}}</h2>
        <p>{{car.year}}</p>
        <p>{{car.price}}</p>
        <button @click="showContact">Show contact</button>
        <RouterView />
    </div>
    <div v-else>
        <h1>Car not found!</h1>
    </div>
</template>