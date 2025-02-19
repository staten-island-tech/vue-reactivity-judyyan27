<template>
  <div class="card">
    <h2 class="name">{{ name }}</h2>
    <p class="price">Price: ${{ price }}</p>
    <img :src="image" :alt="name" class="image" />
    <button @click="addTocart">Add to Cart</button>
  </div>
</template>

<script setup>
defineProps({
  name: String,
  price: String,
  image: String,
})
</script>

<style scoped>
.card {
  border-radius: 1.5rem;
  border-width: 1rem;
  width: 25rem;
  height: 45rem;
  margin: 1rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  border: 1rem groove;
  border-color: black;
}

button {
  padding: 0.3rem;
  font-size: 1.6rem;
  background-color: transparent;
}

.name {
  font-size: 2.5rem;
  color: rgb(13, 54, 51);
  margin-left: 0.3rem;
}

.price {
  font-size: 2rem;
  color: rgb(13, 107, 101);
}

.image {
  height: 25rem;
  width: fit-content;
  object-fit: contain;
  margin: 0.3rem;
}
</style>
