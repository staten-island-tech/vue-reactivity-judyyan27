<template>
    <div class="card">
      <h2>{{ name }}</h2>
      <p>Price: ${{ price }}</p>
      <img :src="image" :alt="name" />
    </div>
  </template>
  
  <script setup>
  defineProps({
    name: String,
    price: Number,
    image: String
  });
  </script>

<!-- <template>
  <div class="flex flex-wrap gap-4 justify-center">
    <IceCreamCard
      v-for="iceCream in iceCreams"
      :key="iceCream.name"
      :name="iceCream.name"
      :price="iceCream.price"
      :image="iceCream.image"
    />
  </div>
</template>

<script setup>
import { ref } from "vue";
import IceCreamCard from "./components/IceCreamCard.vue";

// Sample ice cream data
const iceCreams = ref([
  { name: "Vanilla", price: 2.99, image: "https://via.placeholder.com/100?text=Vanilla" },
  { name: "Chocolate", price: 3.49, image: "https://via.placeholder.com/100?text=Chocolate" },
  { name: "Strawberry", price: 3.29, image: "https://via.placeholder.com/100?text=Strawberry" },
  { name: "Mint Chip", price: 3.59, image: "https://via.placeholder.com/100?text=Mint+Chip" }
]);
</script>

