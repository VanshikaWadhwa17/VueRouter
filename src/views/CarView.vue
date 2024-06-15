<script setup>
import {useRoute , useRouter, RouterView} from "vue-router"
import cars from "../data/cars.json"

const route =useRoute()
//console.log(route.params)
// useRoute allows us to extract information about the current path that we are in
// useRouter allows us to make adjustments/modifiactions in our path
const router= useRouter()
const carId=route.params.id


const car= cars.find(c=>c.id===parseInt(carId))

</script>
<template>
    <div>
       <h1>Car view</h1>
        <p>{{ car.name }}</p>
        <p>{{ car.year }}</p>
        <p>{{ car.price }}</p>
        <button @click="router.push(`/cars/${carId}/contact`)">Contact Dealer</button>
        <RouterView/>
    </div>
</template>