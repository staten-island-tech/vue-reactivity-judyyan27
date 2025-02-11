<template>
  <div class="card">
    <h2 class="name">{{ name }}</h2>
    <p class="price">Price: ${{ price }}</p>
    <img :src="image" :alt="name" class="image" />
    <button @click="addTocart">Add to Cart</button>
    <slot></slot>
  </div>
</template>

<script setup>
import cart from '../components/ShoppingCart.vue'

import { ref } from 'vue'

function addTocart() {
  cart.push(card.name.value)
}

// Button needs to be the child of card and when button is pressed, a function imports the ice cream description to the card -- display the item and add to the total

//Use slots***

defineProps({
  name: String,
  price: Number,
  image: String,
})
</script>

<style scoped>
.card {
  border-radius: 1.5rem;
  border-width: 1rem;
  width: fit-content;
  height: fit-content;
  margin: 1rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  border: 1rem groove;
  border-color: black;
}

.name {
  font-size: 2rem;
}

.price {
  font-size: 2rem;
}

.image {
  height: 40rem;
  width: 30rem;
  object-fit: contain;
  margin: 0.3rem;
}
</style>
