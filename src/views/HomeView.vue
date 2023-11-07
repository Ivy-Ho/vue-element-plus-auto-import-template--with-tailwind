<script setup>
import { useCounterStore } from '@/stores/counter'
const counterStore = useCounterStore()
</script>

<template>
  <main class="flex flex-col space-y-5">
    <section>
      <h2 class="mb-2">Tailwind style testing:</h2>
      <p class="text-xl font-semibold text-orange-500">Hello!</p>
    </section>
    <section>
      <h2 class="mb-2">Element-plus testing:</h2>
      <el-button type="primary">Primary</el-button>
      <el-button type="success" plain>Success</el-button>
    </section>
    <section>
      <h2 class="mb-2">pinia store testing:</h2>
      <p class="mb-2 text-xl text-red-500">Count:{{ counterStore.count }}</p>
      <p class="mb-2 text-xl text-red-500">Double Count:{{ counterStore.doubleCount }}</p>
      <el-button @click="counterStore.increment" plain>Increment</el-button>
    </section>
  </main>
</template>
