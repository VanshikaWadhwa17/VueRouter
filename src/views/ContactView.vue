<script setup>
import {useRoute} from "vue-router"
import cars from "../data/cars.json"
const route = useRoute()
const car= cars.find(c=>c.id===parseInt(route.params.id))
</script>
<template>
    <div v-if="car">
        <h1>Contact View</h1>
        <p>{{ car.contact.dealer }}</p>
        <p>{{ car.contact.number }}</p>
    </div>
    <div v-else>
        <h1>Car and contact not found</h1>
    </div>
</template>