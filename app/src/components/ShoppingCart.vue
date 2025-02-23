<template>
  <div class="cart">
    <h2>Shopping Cart:</h2>
    <h2>-----------------</h2>
    <ul>
      <li v-for="(item, index) in cart" :key="index">
        <span> {{ item.name }} - ${{ item.price }} </span>
        <button @click="deleteItem(index)">Remove Item</button>
      </li>
    </ul>
    <h3>Total Cost: ${{ price }}</h3>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const price = ref('0.00')

const deleteItem = (index) => {
  console.log(index, '-delete item function')
  item.value.splice(index, 1)
}

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
