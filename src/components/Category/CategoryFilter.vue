<script setup>
const props = defineProps({
  type: {
    type: String,
    required: true,
  },
  options: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <div>
    <label class="block font-medium mb-1">{{ props.type }}</label>
    <select class="w-full border px-3 py-2 rounded">
      <option v-for="option in props.options" :key="option">{{ option }}</option>
    </select>
  </div>
</template>
