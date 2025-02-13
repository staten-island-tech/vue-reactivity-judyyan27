<template>
  <div class="cart">
    <h2>Shopping Cart of Ice Cream:</h2>
    <li>{{ cart }}</li>
  </div>
  <div></div>
</template>

<script setup>
import cart from '../components/IceCreamCard.vue'
console.log(cart)

defineProps({
  name: String,
  price: Number,
})
</script>

<style scoped>
.cart {
  width: 40rem;
  height: 30rem;
}
</style>
