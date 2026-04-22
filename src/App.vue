<template>
  <div class="app-shell">
    <AppHeader />

    <main class="shell-main">
      <RouterView />
    </main>

    <AppFooter />
  </div>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import AppFooter from './components/AppFooter.vue'
import AppHeader from './components/AppHeader.vue'
</script>

<style scoped>
.app-shell {
  min-height: 100dvh;
  display: grid;
  grid-template-rows: auto 1fr auto;
}

.shell-main {
  padding-bottom: 0.5rem;
}
</style>
