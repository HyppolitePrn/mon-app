<script setup>
import ProductCard from './ProductCard.vue'

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
  <section class="py-12">
    <div class="max-w-7xl mx-auto px-4">
      <h3 class="text-2xl font-semibold mb-8 text-center">Produits en vedette</h3>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        <ProductCard
          v-for="(product, index) in products"
          :key="index"
          :title="product.title"
          :price="product.price"
          :description="product.description"
        />
      </div>
    </div>
  </section>
</template>
