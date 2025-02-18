<template>
  <div class="card-container">
    <IceCreamCard name="Vanilla" price="1.99" image="vanilla_icecream.png" />
    <IceCreamCard name="Chocolate" price="2.00" image="chocolate.png" />
    <IceCreamCard name="Strawberry" price="2.00" image="strawberry.png" />
    <IceCreamCard name="Cookies and Cream" price="2.50" image="cookiesncream.png" />
    <IceCreamCard name="Mint Chocolate Chip" price="2.25" image="mintchoco.png" />
    <IceCreamCard name="Chocolate Chip" price="2.00" image="choco_chip.webp" />
    <IceCreamCard name="Coffee" price="2.25" image="coffee.png" />
    <IceCreamCard name="Neapolitan" price="2.50" image="neo.png" />
  </div>
</template>

<script setup>
import { reactive } from 'vue'
import IceCreamCard from './IceCreamCard.vue'
import ShoppingCart from './ShoppingCart.vue'

const cart = reactive([])

const handleAddToCart = (item) => {
  cart.push(item) // Add item to cart
  console.log('Cart updated:', cart)
}
</script>

<style scoped>
.card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  flex-direction: row;
  width: 100rem;
  height: 80rem;
}
</style>
