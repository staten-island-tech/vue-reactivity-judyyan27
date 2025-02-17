<template>
  <div>
    <h2>Cart:</h2>
    <ul>
      <li v-for="(item, index) in cart" :key="index">{{ item.name }} - ${{ item.price }}</li>
    </ul>
  </div>
</template>

<script setup>
// Store selected items in cart
const cart = ref([])

// Function to add item to cart
const handleAddToCart = (item) => {
  cart.value.push(item)
  console.log('Cart:', cart.value)
}

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
  background-color: azure;
}
</style>
