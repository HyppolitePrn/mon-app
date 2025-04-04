<script setup>
import CartCard from '@/components/CartCard.vue'
import { computed, ref } from 'vue'

const cartItems = ref([
  {
    id: 1,
    name: 'Chaussures de Ville',
    price: 99.99,
    quantity: 1,
    image: 'https://example.com/image1.jpg',
  },
  {
    id: 2,
    name: 'Baskets Sport',
    price: 79.99,
    quantity: 2,
    image: 'https://example.com/image2.jpg',
  },
])

let totalPrice = computed(() => {
  let result = 0
  for (let item of cartItems.value) {
    result += item.price * item.quantity
  }
  return result.toFixed(2)
})

function deleteItem(index) {
  cartItems.value.splice(index, 1)
}
</script>

<template>
  <main class="max-w-4xl mx-auto px-4 py-10">
    <h2 class="text-2xl font-bold mb-6">Mon Panier</h2>
    <div class="space-y-6">
      <CartCard
        v-for="item in cartItems"
        :key="item.id"
        :title="item.name"
        :price="item.price"
        :quantity="item.quantity"
        v-on:deleteItem="deleteItem(cartItems.indexOf(item))"
      />
    </div>
    <div class="text-right mt-10">
      <p class="text-lg font-semibold">
        Total : <span class="text-blue-600">{{ totalPrice }} €</span>
      </p>
      <button class="mt-4 bg-blue-600 text-white px-6 py-3 rounded-xl hover:bg-blue-700 transition">
        Commander
      </button>
    </div>
  </main>
</template>
