<template>
  <header class="site-header">
    <div class="brand-block">
      <div class="brand-copy">
        <strong>Projeto Vue</strong>
      </div>
    </div>

    <button
      type="button"
      class="menu-button"
      @click="menuOpen = !menuOpen"
      :aria-expanded="menuOpen"
      aria-label="Abrir ou fechar menu"
    >
      <span></span>
      <span></span>
    </button>

    <nav class="site-nav" :class="{ 'is-open': menuOpen }" aria-label="Navegacao principal">
      <RouterLink to="/" class="nav-link" active-class="active" @click="menuOpen = false">Inicio</RouterLink>
      <RouterLink to="/sobre" class="nav-link" active-class="active" @click="menuOpen = false">Sobre</RouterLink>
    </nav>
  </header>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { RouterLink } from 'vue-router'

const menuOpen = ref(false)
</script>

<style scoped>
.site-header {
  position: sticky;
  top: 0;
  z-index: 30;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  padding: 1rem 1.25rem 1rem 0;
  border-bottom: 1px solid var(--line);
  background: rgba(255, 250, 241, 0.82);
  backdrop-filter: blur(12px);
}

.brand-block {
  display: flex;
  align-items: center;
  gap: 0.9rem;
  padding-left: 1.15rem;
  border-left: 7px solid var(--accent);
}

.brand-mark {
  width: 2.8rem;
  height: 2.8rem;
  display: grid;
  place-items: center;
  border-radius: 50%;
  background: linear-gradient(135deg, var(--accent), var(--accent-2));
  color: #fffaf1;
  font-weight: 700;
  letter-spacing: 0.04em;
}

.brand-copy strong,
.brand-copy span {
  display: block;
}

.brand-copy strong {
  color: var(--ink);
  letter-spacing: 0.03em;
}

.brand-copy span {
  color: var(--ink-soft);
  font-size: 0.82rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
}

.site-nav {
  display: flex;
  align-items: center;
  gap: 0.45rem;
  padding-right: 1.15rem;
}

.nav-link {
  text-decoration: none;
  color: var(--ink);
  border-bottom: 2px solid transparent;
  padding: 0.35rem 0.1rem;
  font-size: 0.95rem;
  transition: 180ms ease;
}

.nav-link:hover,
.nav-link.active {
  color: var(--accent);
  border-color: var(--accent);
}

.menu-button {
  display: none;
  width: 2.8rem;
  height: 2.8rem;
  border: 1px solid var(--line);
  border-radius: 50%;
  background: rgba(255, 250, 241, 0.96);
  cursor: pointer;
}

.menu-button span {
  display: block;
  width: 1rem;
  height: 2px;
  margin: 0.23rem auto;
  border-radius: 999px;
  background: var(--ink);
}

@media (max-width: 760px) {
  .site-header {
    flex-wrap: wrap;
  }

  .menu-button {
    display: inline-block;
  }

  .site-nav {
    display: none;
    width: 100%;
    flex-direction: column;
    align-items: stretch;
    padding-top: 0.4rem;
  }

  .site-nav.is-open {
    display: flex;
  }

  .nav-link {
    width: 100%;
    text-align: center;
    padding: 0.75rem 0;
    border-bottom: 1px solid var(--line);
  }
}
</style>
