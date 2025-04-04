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
  quantity: {
    type: Number,
    required: true,
  },
})
const emit = defineEmits(['deleteItem'])
const deleteItem = () => {
  emit('deleteItem')
}
</script>

<template>
  <div class="flex items-center justify-between border-b pb-4">
    <div class="flex items-center gap-4">
      <img
        src="https://via.placeholder.com/100"
        class="w-20 h-20 object-cover rounded"
        alt="Produit"
      />
      <div>
        <p class="font-medium">{{ props.title }}</p>
        <p class="text-gray-500 text-sm">Quantité : {{ props.quantity }}</p>
      </div>
    </div>
    <div class="text-right">
      <p class="font-bold">{{ props.price }} €</p>
      <button class="text-red-500 text-sm hover:underline mt-1" v-on:click="deleteItem">
        Supprimer
      </button>
    </div>
  </div>
</template>
