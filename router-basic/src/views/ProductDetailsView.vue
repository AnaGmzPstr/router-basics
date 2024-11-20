<script setup>
import products from '../assets/productos.json'
import { RouterLink } from 'vue-router'


</script>

<template>
    <div class="productDetail">
        <h1>Details product id: {{ $route.params.id }}</h1>
        <h2>{{ products[$route.params.id - 1].name }}</h2>
        <p>{{ products[$route.params.id - 1].description }}</p>
        <!-- Volver a ProductList.vue -->
        <RouterLink to="/products">Return to Products</RouterLink>
    </div>
</template>

<style scoped>
h1 {
    text-decoration: underline;
}

.productDetail {
    display: flex;
    flex-direction: column;
    align-items: center;
    background: rgba(255, 255, 255, 0.1);
    /* Capa semi-transparente */
    border-radius: 15px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    /* Sombra suave */
    backdrop-filter: blur(10px);
    /* Efecto desenfoque */
    -webkit-backdrop-filter: blur(10px);
    /* Soporte para navegadores webkit */
    border: 1px solid rgba(255, 255, 255, 0.3);
    /* Bordes suaves */
    margin: 2em;
    padding: 2em;

}
</style>