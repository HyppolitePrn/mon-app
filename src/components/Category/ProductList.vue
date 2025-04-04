<script setup>
import ProductCard from '../Home/ProductCard.vue'

const products = [
  { title: 'Sneakers', price: '89,99 €', description: 'Sneakers for everyday wear' },
  {
    title: 'Chaussure Classique',
    price: '12 €',
    description: 'Classic shoes for formal occasions',
  },
  { title: "Bottes d'hiver", price: '99,99 €', description: 'Warm winter boots for cold weather' },
]
</script>

<template>
  <section class="flex-1">
    <h2 class="text-xl font-semibold mb-6">Chaussures pour Homme</h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
      <ProductCard
        v-for="product in products"
        :key="product.title"
        :title="product.title"
        :price="product.price"
        :description="product.description"
      />
    </div>
  </section>
</template>
