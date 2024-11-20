<script setup>
    import productList from '@/assets/productos.json'
    import { RouterLink } from 'vue-router';
</script>
<template>
    <div class="container">

        <h2>Product List</h2>
        <ul>
            <li v-for="product in productList" :key="product.id">
                <RouterLink 
                :to="'/productDetail/' + product.id"
                class="link">
                {{ product.name }}</RouterLink>
            </li>
        </ul>
    </div>
</template>

<style scoped>
.container{
    max-width: 700px;
    margin: 40px auto;
}
li{
    list-style:none;
}

.link{
    text-decoration: none;
    color: #333;
}
.link:hover{
    color: #666;
    text-decoration: underline;
}

</style>