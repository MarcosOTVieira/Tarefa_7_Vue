<template>
  <footer class="site-footer">
    <div class="footer-brand">
      <strong>Tarefa 7 Vue</strong>
    </div>

    <div class="footer-meta">
      <p>Marcos Vieira · Victor Rosseto · Guilherme Goncalves</p>
    </div>

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
  padding: 1rem 1.15rem;
  border-top: 1px solid var(--line);
  background: rgba(255, 250, 241, 0.9);
}

.footer-brand {
  display: grid;
  gap: 0.1rem;
}

.footer-brand strong {
  color: var(--ink);
  letter-spacing: 0.03em;
}

.footer-brand span,
.footer-meta p,
.site-footer span {
  color: var(--ink-soft);
}

.footer-brand span {
  text-transform: uppercase;
  letter-spacing: 0.12em;
  font-size: 0.72rem;
}

.footer-meta p {
  margin: 0;
  text-align: center;
}

.site-footer span {
  white-space: nowrap;
}

@media (max-width: 760px) {
  .site-footer {
    text-align: center;
    flex-direction: column;
  }
}
</style>
