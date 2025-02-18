<template>
  <div class="cart">
    <h2>Shopping Cart:</h2>
    <ul>
      <li v-for="(item, index) in cart" :key="index">{{ item.name }} - ${{ item.price }}</li>
    </ul>
  </div>
</template>

<script setup>
defineProps({
  cart: Array, // Receives cart data from IceCreamList.vue
})
</script>

<style scoped>
h2 {
  text-align: left;
  color: blueviolet;
  font-size: 2.5rem;
}
</style>
