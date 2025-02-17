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
  price: Number,
  image: String,
})

const emit = defineEmits(['addToCart'])
const addToCart = () => {
  emit('addToCart', {
    name: props.name,
    price: props.price,
    image: props.image,
  })
}
</script>

<style scoped>
h2,
p {
  color: darkkhaki;
}

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

.name {
  font-size: 2rem;
}

.price {
  font-size: 2rem;
}

.image {
  height: 25rem;
  width: fit-content;
  object-fit: contain;
  margin: 0.3rem;
}
</style>
