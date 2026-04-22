<template>
  <section class="about-wrap">
    <section class="about-banner">
      <p class="eyebrow">Sobre</p>
      <div class="about-grid">
        <div>
          <h1>Não há nada aqui</h1>
        </div>
      </div>
    </section>
  </section>
</template>

<style scoped>
.about-wrap {
  padding: 2rem 1.1rem;
  display: grid;
  gap: 1rem;
}

.about-banner,
.panel {
  max-width: 980px;
  width: 100%;
  margin: 0 auto;
  border: 1px solid var(--line);
  background: rgba(255, 250, 241, 0.9);
  box-shadow: 0 18px 38px rgba(39, 31, 23, 0.08);
}

.about-banner {
  padding: 1.25rem;
}

.eyebrow {
  display: inline-flex;
  padding: 0.35rem 0.75rem;
  border-radius: 999px;
  background: rgba(32, 88, 243, 0.12);
  color: var(--accent);
  text-transform: uppercase;
  letter-spacing: 0.14em;
  font-size: 0.72rem;
  font-weight: 700;
}

.about-grid {
  display: grid;
  grid-template-columns: minmax(0, 1.2fr) minmax(0, 0.9fr);
  gap: 1rem;
  margin-top: 1rem;
}

.about-grid h1 {
  margin: 0;
  color: var(--ink);
  font-size: clamp(2.2rem, 5vw, 4rem);
  line-height: 0.96;
  max-width: 10ch;
}

.about-grid p {
  margin: 0;
  color: var(--ink-soft);
  max-width: 34ch;
  line-height: 1.7;
  font-size: 1.02rem;
}

.about-panels {
  max-width: 980px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0.9rem;
}

.panel {
  padding: 1.1rem;
  border-radius: 1.1rem;
}

.panel span {
  display: inline-block;
  margin-bottom: 0.7rem;
  text-transform: uppercase;
  letter-spacing: 0.14em;
  font-size: 0.72rem;
  color: var(--ink-soft);
}

.panel h2 {
  margin: 0;
  color: var(--ink);
  font-size: 1.15rem;
  line-height: 1.35;
}

.panel-blue {
  background: linear-gradient(160deg, #e7efff, #fffaf1);
}

.panel-rose {
  background: linear-gradient(160deg, #ffe6df, #fffaf1);
}

.panel-green {
  background: linear-gradient(160deg, #e5f5ee, #fffaf1);
}

@media (max-width: 760px) {
  .about-grid,
  .about-panels {
    grid-template-columns: 1fr;
  }

  .about-grid h1 {
    max-width: none;
  }
}
</style>
