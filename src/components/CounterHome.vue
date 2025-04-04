<script setup lang="ts">
import { ref } from 'vue'

interface Counter {
  id: number
  count: number
}

const counters = ref<Counter[]>([])

function increment(id: number): void {
  const counter = counters.value.find((counter) => counter.id === id)
  if (counter) {
    counter.count++
  }
}

function decrement(id: number): void {
  const counter = counters.value.find((counter) => counter.id === id)
  if (counter) {
    counter.count--
  }
}

function addCounter(): void {
  counters.value.push({
    count: 0,
    id: counters.value.length + 1,
  })
}
</script>

<template>
  <main>
    <div
      class="flex flex-col gap-4 border-2 border-gray-300 rounded-md m-4"
      v-for="{ count, id } in counters"
      :key="id"
    >
      <h1>Compteur: {{ count }}</h1>
      <h2>Compteur {{ id }}</h2>
      <button class="bg-red-500 text-white px-4 py-2 rounded" @click="increment(id)">
        Incrémenter
      </button>
      <button class="bg-red-500 text-white px-4 py-2 rounded" @click="decrement(id)">
        Décrémenter
      </button>
    </div>
    <button class="bg-red-500 text-white px-4 py-2 rounded" @click="addCounter">
      Ajouter un compteur
    </button>
  </main>
</template>
