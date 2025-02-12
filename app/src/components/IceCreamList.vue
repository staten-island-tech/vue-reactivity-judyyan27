<template>
  <div class="card-container">
    <IceCreamCard name="Vanilla" price="1.99" image="vanilla_icecream.png" />
    <IceCreamCard name="Chocolate" price="2.00" image="chocolate.png" />
    <IceCreamCard name="Strawberry" price="2.00" image="strawberry.png" />
    <IceCreamCard name="Cookies and Cream" price="2.50" image="cookiesncream.png" />
    <IceCreamCard name="Mint Chocolate Chip" price="2.25" image="mintchoco.png" />
    <IceCreamCard name="Coffee" price="2.25" image="coffee.png" />
    <IceCreamCard name="Neapolitan" price="2.50" image="neo.png" />
  </div>
</template>

<script setup>
import IceCreamCard from '../components/IceCreamCard.vue'
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
