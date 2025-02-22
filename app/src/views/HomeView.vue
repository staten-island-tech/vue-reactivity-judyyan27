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
.container {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  padding: 1rem;
}

.cards {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  width: 80%;
}

.cart {
  height: 140rem;
  background-color: azure;

  padding: 0.5rem;
}
</style>
