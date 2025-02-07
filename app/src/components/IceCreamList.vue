<template>
  <div class="card-container">
    <IceCreamCard name="Vanilla" price="2.99" image="vanilla_icecream.png" />
    <IceCreamCard name="Chocolate" price="2.99" image="vanilla_icecream.png" />
    <IceCreamCard name="Strawberry" price="2.99" image="vanilla_icecream.png" />
    <IceCreamCard name="Cookies and Cream" price="2.99" image="vanilla_icecream.png" />
    <IceCreamCard name="Mint Chocolate Chip" price="2.99" image="vanilla_icecream.png" />
    <IceCreamCard name="Coffee" price="2.99" image="vanilla_icecream.png" />
    <IceCreamCard name="Neapolitan" price="2.99" image="vanilla_icecream.png" />
  </div>
</template>

<script setup>
import IceCreamCard from './components/IceCreamCard.vue'
</script>

<style scoped>
.card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  flex-direction: row;
}
</style>
