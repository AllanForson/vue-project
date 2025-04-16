<template>
  <div class="product-card">
    <img :src="product.image" :alt="product.name" class="product-image" />
    <h2 class="product-name">{{ product.name }}</h2>
    <p class="product-price">${{ product.price }}</p>
    <button class="add-to-cart" @click="addToCart">Add to Cart</button>
  </div>
</template>

<script lang="ts">
export default {
  name: 'ProductCard',
  data() {
    return {
      product: {
        name: 'Random T-Shirt',
        price: (Math.random() * 50 + 10).toFixed(2),
        image: 'https://via.placeholder.com/150',
      },
    }
  },
  methods: {
    addToCart() {
      alert(`${this.product.name} has been added to your cart!`)
    },
  },
}
</script>
