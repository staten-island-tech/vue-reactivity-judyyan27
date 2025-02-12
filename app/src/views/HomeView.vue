<script setup>
import IceCreamList from '@/components/IceCreamList.vue'
import ShoppingCart from '@/components/ShoppingCart.vue'
</script>

<template>
  <div class="container"><IceCreamList /></div>
  <div><ShoppingCart /></div>
</template>

<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  flex-direction: row;
}
</style>
