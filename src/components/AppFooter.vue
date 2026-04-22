<template>
  <footer class="site-footer">
    <div>
      <strong>Tarefa 7 Vue / Angular</strong>
    </div>

    <ul>
      <li>Marcos Vieira</li>
      <li>Victor Rosseto</li>
      <li>Guilherme Goncalves</li>
    </ul>

    <span>UniFacens {{ currentYear }}</span>
  </footer>
</template>

<script setup lang="ts">
const currentYear = new Date().getFullYear()
</script>

<style scoped>
.site-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  padding: 1rem 1.1rem;
  border-top: 1px solid var(--ui-border);
  background: color-mix(in oklab, var(--paper) 88%, white 12%);
}

.site-footer strong {
  color: var(--ink);
}

.site-footer p {
  margin: 0.3rem 0 0;
  color: var(--ink-soft);
}

.site-footer ul {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 0.45rem 0.9rem;
  margin: 0;
  padding: 0;
  color: var(--ink-soft);
}

.site-footer span {
  color: var(--ink-soft);
  white-space: nowrap;
}

@media (max-width: 760px) {
  .site-footer {
    text-align: center;
    flex-direction: column;
  }
}
</style>
