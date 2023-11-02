<script setup>
import { useCounterStore } from '@/stores/counter'
const counter = useCounterStore()
</script>

<template>
  <h2>Tailwind style testing:</h2>
  <p class="mb-3 text-lg font-semibold text-orange-500">Hello!</p>
  <h2>Element-plus testing:</h2>
  <el-button type="primary">Primary</el-button>
  <el-button type="success" plain>Success</el-button>
  <h2 class="mt-3">Pinia store testing:</h2>
  <p>{{ counter.text }}</p>
</template>
