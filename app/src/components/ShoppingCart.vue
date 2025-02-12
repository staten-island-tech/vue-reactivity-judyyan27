<template>
  <div>
    <h2>Shopping Cart of Ice Cream:</h2>
    <li>{{ cart }}</li>
  </div>
  <div></div>
</template>

<script setup>
import cart from '../components/IceCreamCard.vue'
console.log(cart)
</script>

<style scoped></style>
