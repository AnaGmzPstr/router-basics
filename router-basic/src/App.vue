<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  
  <header>
    <nav>
      <RouterLink class="link" to="/">Home</RouterLink>
      <RouterLink class="link" to="/about">About</RouterLink>
      <RouterLink class="link" to="/contact">Contact</RouterLink>
      <RouterLink class="link" to="/products">Products</RouterLink>
    </nav>
  </header>
  <RouterView />
</template>

<style scoped>
*{
  padding: 0;
  margin: 0;
}
header{
  background-color: #333;
  color: #fff;
  padding: 1rem;
  text-align: center;
  margin: 0;
}
nav{
  padding: 1rem;
}

.link{
  color: antiquewhite;
  text-decoration: none;
  margin: 0 1rem;
  transition: ease-in-out .3s;
}

.link:hover{
  text-decoration: underline;
  color: #fff;
}

</style>
