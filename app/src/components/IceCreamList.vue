<template>
  <div class="container">
    <div class="card-container">
      <IceCreamCard
        v-for="(item, index) in shop"
        :key="index"
        :name="item.name"
        :price="item.price"
        :image="item.image"
        :index="item.index"
        v-on:AddtoCart="addingitem"
      />
    </div>

    <div class="cart">
      <h2>Shopping Cart:</h2>
      <h2>---------------</h2>
      <p v-for="(item, index) in cart" :key="index">
        <span> {{ item.name }} - ${{ item.price }} </span>
        <button @click="deleteItem(index)">Remove Item</button>
      </p>
      <h3>Total Cost: ${{ totalPrice.toFixed(2) }}</h3>
    </div>
  </div>
</template>

<script setup>
import IceCreamCard from './IceCreamCard.vue'
import { ref, computed, onUpdated } from 'vue'

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

const cart = ref([])

// Add item to cart
function addingitem(index) {
  console.log(index, '- Adding item to cart')
  const item = shop.value[index] // Get the item from the shop array
  if (item) {
    cart.value.push({ name: item.name, price: item.price }) // Append item to cart
  }
}

// Remove item from cart
const deleteItem = (index) => {
  cart.value.splice(index, 1)
}

// Compute total price dynamically
const totalPrice = computed(() => {
  return cart.value.reduce((sum, item) => sum + item.price, 0)
})

// Runs every time cart updates
onUpdated(() => {
  console.log('Cart updated:', cart.value)
})
</script>

<!-- <template>
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
import IceCreamCard from './IceCreamCard.vue'
import { onUpdated, ref } from 'vue'

defineProps({
  cart: Array,
})

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

const price = ref('0.00')

function displayCart() {}

const deleteItem = (index) => {
  console.log(index, '-delete item function')
  item.value.splice(index, 1)
}
</script> -->

<style scoped>
.card-container {
  width: 80%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  flex-direction: row;
  width: 100rem;
  height: 80rem;
  align-self: flex-start;
}

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

p {
  padding: 0.2rem;
  text-align: left;
  font-size: 3rem;
  color: rgb(54, 17, 23);
}

.cart {
  height: 140rem;
  width: 25%;
  background-color: azure;
  padding: 0.5rem;
}

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
  width: 75%;
}
</style>
