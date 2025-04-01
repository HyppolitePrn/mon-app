<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  price: {
    type: Number,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="border rounded-2xl overflow-hidden shadow hover:shadow-md transition">
    <img src="../../assets/logo.svg" alt="Chaussure" class="w-full h-60 object-cover" />
    <div class="p-4">
      <h4 class="font-semibold text-lg">{{ props.title }}</h4>
      <p class="text-gray-600">{{ props.description }}</p>
      <p class="font-bold mt-2">{{ props.price }} €</p>
    </div>
  </div>
</template>
