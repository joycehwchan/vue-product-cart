<template>
  <main class="wrapper">
    <h1>Products</h1>

    <div class="card-container">
      <ProductCard
        v-for="(product, index) in inventory"
        :index="index"
        :product="product"
        :addToCart="addToCart"
        :key="product.id"
      />
    </div>
  </main>
</template>

<script>
import ProductCard from '../components/ProductCard.vue'

export default {
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
}
</script>
