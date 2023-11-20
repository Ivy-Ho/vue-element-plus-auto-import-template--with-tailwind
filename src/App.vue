<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="p-[20px]">
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </nav>

    <RouterView />
  </div>
</template>
<style lang="scss" scoped>
nav {
  margin-bottom: 20px;
  a {
    display: inline-block;
    padding: 0 1rem;
    border-left: 2px solid #ddd;
    &:hover {
      color: orange;
    }
  }
  a.router-link-exact-active {
    color: orange;
  }
}
</style>
