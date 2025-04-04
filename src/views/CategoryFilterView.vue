<script setup>
import CategoryFilter from '@/components/Category/CategoryFilter.vue'
import ProductList from '@/components/Category/ProductList.vue'
</script>

<template>
  <main class="max-w-7xl mx-auto px-4 py-10">
    <div class="flex flex-col md:flex-row gap-8">
      <aside class="md:w-1/4">
        <h2 class="text-lg font-semibold mb-4">Filtres</h2>

        <div class="space-y-4">
          <CategoryFilter :type="'genre'" :options="['Tous', 'Homme', 'Femme']" />
          <CategoryFilter :type="'prix'" :options="['0-50 €', '50-100 €', '100-150 €']" />
        </div>
      </aside>
      <ProductList />
    </div>
  </main>
</template>
