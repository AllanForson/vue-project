<script lang="ts">
import ProductCard from '@/components/Home/ProductCard.vue'

export default {
  name: 'PopularProducts',
  components: {
    ProductCard,
  },
  data() {
    return {
      products: [
        {
          id: 1,
          name: 'Wireless Headphones',
          price: '$99.99',
          image: 'headphones.jpg',
        },
        {
          id: 2,
          name: 'Smart Watch',
          price: '$199.99',
          image: 'smartwatch.jpg',
        },
        {
          id: 3,
          name: 'Gaming Mouse',
          price: '$49.99',
          image: 'mouse.jpg',
        },
        {
          id: 4,
          name: 'Mechanical Keyboard',
          price: '$89.99',
          image: 'keyboard.jpg',
        },
      ],
    }
  },
}
</script>

<template>
  <div class="popular-products">
    <h2>Popular Products</h2>
    <div class="products-grid">
      <ProductCard
        v-for="product in products"
        :key="product.id"
        :name="product.name"
        :price="product.price"
        :image="product.image"
      />
    </div>
  </div>
</template>

<style scoped>
.popular-products {
  padding: 20px;
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 20px;
}
</style>
