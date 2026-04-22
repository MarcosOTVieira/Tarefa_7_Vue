<template>
  <section class="page-wrap">
    <section class="poster">
      <div class="poster-labels">
        <span>Home</span>
        <span>Vue · Tarefa 7</span>
      </div>

      <div class="poster-layout">
        <div class="poster-copy">
          <p class="kicker">Tarefa 7 WD</p>
          <h1>Um layout basico</h1>
          <p class="lead">
            A ideia foi fazer um site simples, com uma pegada mais editorial, usando os componentes de header e footer
          </p>
        </div>
        </div>
    </section>
  </section>
</template>

<style scoped>
.page-wrap {
  padding: 2rem 1.1rem;
  min-height: calc(100dvh - 220px);
  display: grid;
  gap: 1.2rem;
}

.poster,
.strip {
  width: 100%;
  border: 1px solid var(--line);
  background: rgba(255, 250, 241, 0.88);
  box-shadow: 0 18px 38px rgba(39, 31, 23, 0.08);
}

.poster {
  max-width: 1080px;
  margin: 0 auto;
  padding: 1rem;
  position: relative;
  overflow: hidden;
}

.poster::before {
  content: '';
  position: absolute;
  inset: 0;
  background:
    linear-gradient(135deg, rgba(32, 88, 243, 0.06) 0 34%, transparent 34% 100%),
    radial-gradient(circle at 86% 18%, rgba(239, 91, 63, 0.14), transparent 20%);
  pointer-events: none;
}

.poster-labels {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  margin-bottom: 1.1rem;
  color: var(--ink-soft);
  text-transform: uppercase;
  letter-spacing: 0.12em;
  font-size: 0.73rem;
}

.poster-layout {
  position: relative;
  display: grid;
  grid-template-columns: minmax(0, 1.55fr) minmax(220px, 0.65fr);
  gap: 1rem;
  align-items: stretch;
}

.poster-copy {
  padding: 1.35rem 1.35rem 1.35rem 1rem;
}

.kicker {
  margin: 0 0 0.65rem;
  color: var(--accent-2);
  text-transform: uppercase;
  letter-spacing: 0.15em;
  font-size: 0.74rem;
  font-weight: 700;
}

.poster-copy h1 {
  margin: 0;
  color: var(--ink);
  font-size: clamp(2.6rem, 7vw, 5.4rem);
  line-height: 0.92;
  max-width: 9ch;
}

.lead {
  margin-top: 1rem;
  max-width: 46ch;
  color: var(--ink-soft);
  line-height: 1.8;
  font-size: 1.02rem;
}

.poster-slab {
  display: grid;
  align-content: end;
  gap: 0.8rem;
  padding: 1rem;
  min-height: 260px;
  border-radius: 1.4rem 0.5rem 1.4rem 0.5rem;
}

.poster-slab strong {
  color: #fffaf1;
  font-size: 3.2rem;
  line-height: 1;
}

.poster-slab p {
  color: rgba(255, 250, 241, 0.92);
  margin: 0;
  max-width: 14ch;
  font-size: 1.15rem;
}

.slab-blue {
  background: linear-gradient(160deg, var(--accent), #1239b6);
}

.strip-grid {
  max-width: 1080px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1.1fr 1fr 0.9fr;
  gap: 1rem;
}

.strip {
  padding: 1.15rem;
  border-radius: 1rem;
}

.strip span {
  display: inline-block;
  margin-bottom: 0.7rem;
  text-transform: uppercase;
  letter-spacing: 0.14em;
  font-size: 0.74rem;
  color: var(--ink-soft);
}

.strip p {
  margin: 0;
  color: var(--ink);
  line-height: 1.65;
  font-size: 1.05rem;
}

.slab-cream {
  background: var(--paper-2);
}

.slab-coral {
  background: linear-gradient(160deg, #ffd7cb, #ffefea);
}

.slab-olive {
  background: linear-gradient(160deg, #e8efc8, #f6f8ea);
}

@media (max-width: 900px) {
  .poster-layout,
  .strip-grid {
    grid-template-columns: 1fr;
  }

  .poster-copy {
    padding-right: 0;
  }
}

@media (max-width: 760px) {
  .poster-labels {
    flex-direction: column;
    align-items: flex-start;
  }

  .poster-copy h1 {
    max-width: none;
  }
}
</style>
