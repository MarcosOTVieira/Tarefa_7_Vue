<template>
  <header class="site-header">
    <div class="brand-block">
      <div class="brand-copy">
        <strong>Projeto Vue</strong>
        <span>Tarefa 7</span>
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
  padding: 0.9rem 1.1rem;
  border-bottom: 1px solid var(--ui-border);
  background: color-mix(in oklab, var(--paper) 90%, white 10%);
  backdrop-filter: blur(18px);
}

.brand-block {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.brand-mark {
  width: 2.7rem;
  height: 2.7rem;
  display: grid;
  place-items: center;
  border-radius: 0.85rem;
  background: linear-gradient(135deg, var(--brand-orange), var(--brand-red));
  color: #fff;
  font-weight: 800;
  letter-spacing: 0.08em;
}

.brand-copy strong,
.brand-copy span {
  display: block;
}

.brand-copy span {
  color: var(--ink-soft);
  font-size: 0.82rem;
}

.site-nav {
  display: flex;
  align-items: center;
  gap: 0.6rem;
}

.nav-link {
  text-decoration: none;
  color: var(--ink-soft);
  border: 1px solid transparent;
  border-radius: 999px;
  padding: 0.65rem 0.95rem;
  transition: 180ms ease;
}

.nav-link:hover,
.nav-link.active {
  color: var(--ink);
  border-color: var(--ui-border);
  background: color-mix(in oklab, var(--brand-sand) 22%, white 78%);
}

.menu-button {
  display: none;
  width: 2.8rem;
  height: 2.8rem;
  border: 1px solid var(--ui-border);
  border-radius: 0.75rem;
  background: color-mix(in oklab, var(--paper) 82%, white 18%);
  cursor: pointer;
}

.menu-button span {
  display: block;
  width: 1.1rem;
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
  }
}
</style>
