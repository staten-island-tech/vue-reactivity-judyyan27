[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=17740706)

Project Idea: Dessert themed game or customization webpage

## Ice Cream Cone Customizer--

### The website will consist of a product container of all the available ice cream scoop flavors (vanilla, chocolate, strawberry, etc..)

-- Top Section contains the header
-- A section that was the list of flavors, an image, price, and button to add to cone
-- A visual section that contains the ice cream
-- A section with the total price and list of flavors, clear cart, and remove last item

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
