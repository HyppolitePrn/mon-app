<script setup>
import { RouterView } from 'vue-router'
import Header from '@/components/HeaderComponent.vue'
import Footer from '@/components/FooterComponent.vue'
</script>

<template>
  <Header />
  <RouterView class="max-w-7xl mx-auto px-4 py-10" />
  <Footer />
</template>

<style scoped></style>
