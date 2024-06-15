<script setup>
import {RouterLink} from "vue-router"

</script>
<template>
    <div>
        <RouterLink active-class="active" to="/">Home</RouterLink> 
        <RouterLink active-class="active" to="/about">About</RouterLink> 

        <!-- everytime we click on either of them the page is refreshing and rendering the component that we are routing to - thats a problem --> 
        <!-- we used router link to solve this problem here instead of Anchor tag--> 
    </div>
</template>
<style scoped>
.active{
    font-weight: 900;
    color: rgb(153,104,14)
}</style>