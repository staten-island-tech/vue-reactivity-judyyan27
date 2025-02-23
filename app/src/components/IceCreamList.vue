<template>
  <div class="card-container">
    <IceCreamCard
      v-for="item in shop"
      :name="item.name"
      :price="item.price"
      :image="item.image"
      :index="item.index"
      v-on:AddtoCart="addingitem"
    />
  </div>
</template>

<script setup>
import IceCreamCard from './IceCreamCard.vue'
import { ref } from 'vue'

const cart = ref([])

function addingitem(index) {
  console.log(index, '- Adding item to cart')
  const item = shop.value[index] // Get the item from the shop array
  if (item) {
    cart.value.push({ name: item.name, price: item.price }) // Append item to cart
    console.log(cart.value) // Console.log updated cart
  }
}

let shop = ref([
  {
    name: 'Vanilla',
    price: 1.99,
    image: 'vanilla_icecream.png',
    index: 0,
  },
  {
    name: 'Chocolate',
    price: 2.0,
    image: 'chocolate.png',
    index: 1,
  },
  {
    name: 'Strawberry',
    price: 2.0,
    image: 'strawberry.png',
    index: 2,
  },
  {
    name: 'Cookies and Cream',
    price: 2.5,
    image: 'cookiesncream.png',
    index: 3,
  },
  {
    name: 'Mint Chocolate Chip',
    price: 2.25,
    image: 'mintchoco.png',
    index: 4,
  },
  {
    name: 'Chocolate Chip',
    price: 2.0,
    image: 'choco_chip.webp',
    index: 5,
  },
  {
    name: 'Coffee',
    price: 2.25,
    image: 'coffee.png',
    index: 6,
  },
  {
    name: 'Neapolitan',
    price: 2.5,
    image: 'neo.png',
    index: 7,
  },
])
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
