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
  image: String,
})
</script>
