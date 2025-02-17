<script setup>
import ShopHeader from '@/components/ShopHeader.vue'
import IceCreamList from '@/components/IceCreamList.vue'
import ShoppingCart from '@/components/ShoppingCart.vue'
</script>

<template>
  <div><ShopHeader /></div>
  <div class="container"><IceCreamList /></div>
  <div class="cart"><ShoppingCart /></div>
</template>

<style scoped>
.cart {
  align-items: center;
  flex-wrap: wrap;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background-color: blanchedalmond;
}

.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  flex-direction: row;
}
</style>
