<script setup>
import { useCounterStore } from '@/stores/counter'
const counterStore = useCounterStore()
</script>

<template>
  <main class="flex flex-col space-y-5">
    <section class="w-[300px] rounded-lg bg-gray-200 p-4">
      <h2 class="mb-2 text-[18px] font-semibold">Tailwind style testing:</h2>
      <p class="text-xl font-semibold text-orange-500">Hello!</p>
    </section>
    <section class="w-[300px] rounded-lg bg-gray-200 p-4">
      <h2 class="mb-2 text-[18px] font-semibold">Element-plus testing:</h2>
      <el-button type="primary">Primary</el-button>
      <el-button type="success" plain>Success</el-button>
    </section>
    <section class="w-[300px] rounded-lg bg-gray-200 p-4">
      <h2 class="mb-2 text-[18px] font-semibold">pinia store testing:</h2>
      <p class="mb-2 text-xl text-red-500">Count:{{ counterStore.count }}</p>
      <p class="mb-2 text-xl text-red-500">Double Count:{{ counterStore.doubleCount }}</p>
      <el-button @click="counterStore.increment" plain>Increment</el-button>
    </section>
  </main>
</template>
