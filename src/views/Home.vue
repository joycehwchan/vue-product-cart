<template>
  <div class="home">
    <div class="splash-container">
      <div class="splash">
        <h1>Foodieland</h1>
      </div>
    </div>

    <main class="wrapper">
      <h2>Recommended</h2>

      <div class="recommended">
        <ProductCard
          v-for="(product, index) in inventory.slice(0, 3)"
          :index="index"
          :product="product"
          :addToCart="addToCart"
          :key="product.id"
        />
      </div>
    </main>
  </div>
</template>

<script>
import ProductCard from '../components/ProductCard.vue'
// prettier-ignore
export default {
  name: 'Home',
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
}
</script>
