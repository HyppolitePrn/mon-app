<script setup>
import { ref } from 'vue'

let counters = ref([])

function incrementCounter(counter) {
  counter.value = counter.value + 1
}

function decrementCounter(counter) {
  counter.value = counter.value - 1
}

function addCounter() {
  counters.value.push(ref(0))
}
</script>

<template>
  <main>
    <button class="bg-emerald-400 rounded-md p-1" v-on:click="addCounter">add counter</button>
    <div v-for="(counter, index) in counters" :key="index">
      <div class="bg-green-200 p-1.5 rounded-md">counter: {{ counter }}</div>
      <button class="bg-blue-400 rounded-md m-2 p-2" v-on:click="incrementCounter(counter)">
        incrémenter
      </button>
      <button class="bg-red-400 rounded-md m-2 p-2" v-on:click="decrementCounter(counter)">
        décrémenter
      </button>
    </div>
  </main>
</template>
