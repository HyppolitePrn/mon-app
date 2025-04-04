<script setup>
const menuItems = [
  { name: 'Accueil', href: '/' },
  { name: 'Filtres', href: '/category-filter' },
  { name: 'Homme', href: '/category' },
  { name: 'Produit', href: '/product' },
  { name: 'Panier', href: '/cart' },
]
</script>

<template>
  <header class="border-b shadow-sm sticky top-0 bg-white z-50">
    <div class="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
      <h1 class="text-2xl font-bold">Chaussures Élégance</h1>
      <nav class="space-x-6 hidden md:flex">
        <ul class="flex space-x-6">
          <li v-for="item in menuItems" :key="item.name">
            <a :href="item.href" class="text-gray-600 hover:text-blue-600 transition">
              {{ item.name }}
            </a>
          </li>
        </ul>
      </nav>
      <button class="md:hidden">☰</button>
    </div>
  </header>
</template>
