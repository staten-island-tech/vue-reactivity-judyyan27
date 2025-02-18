<script setup>
import ShopHeader from '@/components/ShopHeader.vue'
import IceCreamList from '@/components/IceCreamList.vue'
import ShoppingCart from '@/components/ShoppingCart.vue'
</script>

<template>
  <div><ShopHeader /></div>
  <div class="container">
    <div class="cards"><IceCreamList /></div>
    <div class="cart"><ShoppingCart /></div>
  </div>
</template>

<style scoped>
/* ✅ Use Flexbox to align items */
.container {
  display: flex;
  justify-content: space-between; /* Pushes cart to the right */
  align-items: flex-start; /* Aligns cart and cards at the top */
  padding: 1rem;
}

/* ✅ Ice cream cards stay on the left */
.cards {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  width: 70%; /* Take most of the space */
}

/* ✅ Shopping cart stays on the right */
.cart {
  width: 30%; /* Takes up only 25% of the screen */
  height: cover;
  background-color: azure;
  padding: 0.5rem;
}
</style>
