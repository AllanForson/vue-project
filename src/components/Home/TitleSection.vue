<template>
  <section class="title-section">
    <div class="container">
      <h1 class="title">Step Into Style</h1>
      <p class="subtitle">Discover the latest and greatest in sneakers, only at ShoeX.</p>
      <button class="shop-now-btn">Shop Now</button>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: 'TitleSection',
}
</script>

<style scoped>
.title-section {
  background: url('@/assets/shoes-banner.jpg') no-repeat center center;
  background-size: cover;
  text-align: center;
  padding: 100px 20px;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.title {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 20px;
}

.subtitle {
  font-size: 1.5rem;
  margin-bottom: 30px;
}

.shop-now-btn {
  background-color: #ff4500;
  color: #fff;
  border: none;
  padding: 15px 30px;
  font-size: 1rem;
  cursor: pointer;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.shop-now-btn:hover {
  background-color: #e03e00;
}
</style>
