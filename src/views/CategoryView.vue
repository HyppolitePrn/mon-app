<script setup>
import SubCategory from '@/components/Category/SubCategory.vue'
</script>

<template>
  <main class="max-w-7xl mx-auto px-4 py-10">
    <h2 class="text-3xl font-bold mb-8 text-center">Chaussures Homme</h2>
    <section class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
      <SubCategory
        :title="'Chaussures de Ville'"
        :description="'Classiques, élégantes pour vos journées de travail'"
      />
    </section>
  </main>
</template>
