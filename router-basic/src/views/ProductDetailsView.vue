<script setup>
import products from '../assets/productos.json'
import { RouterLink } from 'vue-router'


</script>

<template>
    <div class="productDetail">
        <h1>Details product id: {{ $route.params.id }}</h1>
        <h2>{{ products[$route.params.id-1].name }}</h2>
        <p>{{ products[$route.params.id-1].description }}</p>
    </div>
</template>

<style scoped>
h1{
    text-decoration: underline;
}
.productDetail {
    display: flex;
    flex-direction: column;
    align-items: center;
}
</style>