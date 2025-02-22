<template>
  <div class="cart">
    <h2>Shopping Cart:</h2>
    <h2>-----------------</h2>
    <ul>
      <li v-for="(item, index) in cart" :key="index">{{ item.name }} - ${{ item.price }}</li>
    </ul>
    <h3>Total Cost: $</h3>
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
  color: rgb(36, 17, 54);
  font-size: 2.5rem;
}

h3 {
  text-align: left;
  color: rgb(36, 17, 54);
  font-size: 2rem;
}
</style>
