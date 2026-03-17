<template>
  <div id="app" class="theme-wrapper">
    <div class="reading-progress" :style="{ width: scrollProgress + '%' }"></div>

    <!-- Header Editorial -->
    <header class="editorial-header">
      <div class="content-limit">
        <div class="tag-line">Estudos de Gênero • Perspectiva Brasileira</div>
        <h1 class="main-title">A Gramática da <br /><span class="italic">Masculinidade</span></h1>
        <p class="abstract">
          Uma investigação sobre as engrenagens invisíveis que sustentam a hegemonia masculina e as
          suas consequências fatais na vida das mulheres brasileiras.
        </p>
        <div class="scroll-indicator">↓</div>
      </div>
    </header>

    <main class="content-limit">
      <!-- Seção 01: O Dispositivo -->
      <section class="chapter">
        <div class="chapter-info">
          <span class="chapter-number">01</span>
          <h2 class="chapter-title">O Dispositivo de Interpelação</h2>
        </div>

        <div class="two-columns">
          <div class="text-block">
            <p>
              Para <strong>Valeska Zanello</strong>, a masculinidade não é inata, mas um
              "dispositivo". Desde a infância, o homem é <em>interpelado</em> (convocado) a provar
              que não é uma mulher. Essa negação constante do feminino cria uma identidade baseada
              na oposição e no domínio.
            </p>
            <p>
              Trata-se de um sistema de poder. A hegemonia estabelece uma liderança que coloca as
              mulheres em uma posição de subordinação, validando o controle sobre seus corpos,
              desejos e escolhas.
            </p>
          </div>
          <div class="insight-box">
            <p>
              "A masculinidade se constrói, primordialmente, no desprezo e na negação do que é ser
              mulher."
            </p>
          </div>
        </div>
      </section>

      <!-- Seção 02: Teoria de Connell -->
      <section class="chapter grey-area">
        <div class="section-intro">
          <h2 class="sub-title">Dinâmicas do Poder Masculino</h2>
          <p>
            Como a masculinidade se organiza para manter a estrutura de privilégios sobre as
            mulheres.
          </p>
        </div>

        <div class="theory-grid">
          <div
            v-for="(t, index) in teoria"
            :key="t.name"
            :class="['theory-card', { 'full-width': index >= 2 }]"
          >
            <div class="card-content">
              <div class="card-head">
                <span class="card-dot"></span>
                <h3>{{ t.name }}</h3>
              </div>
              <p>{{ t.desc }}</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Seção 03: Destaque Clay -->
      <section class="chapter accent-clay">
        <div class="quote-massive">
          <blockquote>
            "O dividendo patriarcal é o lucro que os homens obtêm da subordinação das mulheres,
            mesmo que não sejam agressores diretos."
          </blockquote>
        </div>

        <div class="reflexion-grid">
          <div class="reflexion-item">
            <h4>A Manutenção do Controle</h4>
            <p>
              O sistema incentiva a vigilância sobre a conduta feminina. O controle não é apenas
              físico, mas simbólico, ditando como a mulher deve se comportar na esfera privada e
              pública.
            </p>
          </div>
          <div class="reflexion-item">
            <h4>O Silenciamento</h4>
            <p>
              A estrutura hegemônica invalida a voz feminina, tratando as demandas das mulheres como
              emocionais ou irrelevantes para manter a autoridade da "razão" masculina.
            </p>
          </div>
        </div>
      </section>

      <!-- Seção 04: Consequências Reais -->
      <section class="chapter">
        <div class="chapter-info">
          <span class="chapter-number">02</span>
          <h2 class="chapter-title">O Impacto na Vida Feminina</h2>
        </div>
        <div class="two-columns">
          <div class="insight-box secondary">
            <p>O Brasil é um dos países que mais mata mulheres no mundo por questões de gênero.</p>
          </div>
          <div class="text-block">
            <p>
              A busca masculina por domínio se reflete em índices alarmantes de violência doméstica.
              Quando a autonomia feminina ameaça a "honra" ou o controle do homem, o dispositivo de
              masculinidade frequentemente responde com agressão.
            </p>
            <p>
              Isso cria um estado de insegurança constante para as mulheres, que precisam adaptar
              suas rotinas, vestimentas e falas para evitar a violência de um sistema que as vê como
              propriedades.
            </p>
          </div>
        </div>
      </section>

      <!-- Seção 05: Dados -->
      <section class="chapter">
        <div class="data-container">
          <div class="data-header">
            <h2>Retrato da Violência Contra a Mulher <span class="year-tag">2023 / 2024</span></h2>
            <p>O feminicídio é o estágio final de um ciclo de controle e poder masculinista.</p>
          </div>

          <div class="stats-row">
            <div class="stat-circle">
              <span class="stat-num">1.467</span>
              <span class="stat-label"
                >Mulheres assassinadas em 2023 (Maior índice registrado)</span
              >
            </div>
            <div class="stat-circle">
              <span class="stat-num">61,1%</span>
              <span class="stat-label">Das vítimas de feminicídio são mulheres negras</span>
            </div>
            <div class="stat-circle">
              <span class="stat-num">1 a cada 6</span>
              <span class="stat-label">Horas uma mulher é morta por ser mulher no Brasil</span>
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer class="main-footer">
      <div class="content-limit">
        <div class="footer-grid">
          <div class="footer-brand">
            <h3>Educação & Gênero</h3>
            <p>Uma ferramenta para conscientização e defesa dos direitos das mulheres.</p>
          </div>
          <div class="footer-source">
            <p class="label">Referência Bibliográfica</p>
            <p>© 2026 — Baseado na obra de Valeska Zanello e Raewyn Connell.</p>
            <p>
              ZANELLO, Valeska.
              <strong
                >Saúde mental, gênero e dispositivos: cultura e processos de subjetivação.</strong
              >
              Curitiba: Appris, 2018.
            </p>
            <p>* Dados baseados no Anuário Brasileiro de Segurança Pública 2024.</p>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const scrollProgress = ref(0)

const teoria = [
  {
    name: 'Hegemonia',
    desc: 'A imposição de um padrão masculino que exige a submissão das mulheres. É a crença de que o homem possui autoridade natural para liderar e decidir por elas.',
  },
  {
    name: 'Subordinação',
    desc: 'A posição imposta às mulheres na estrutura social, onde seus direitos e desejos são secundarizados em relação às necessidades dos homens.',
  },
  {
    name: 'Cumplicidade',
    desc: 'O apoio silencioso de outros homens à opressão feminina. Ao não confrontar comportamentos abusivos, validam a continuidade da violência.',
  },
  {
    name: 'Domínio Territorial',
    desc: 'A ideia de que o corpo feminino e o espaço doméstico pertencem ao homem. No contexto brasileiro, isso se agrava com o racismo, tornando as mulheres negras as principais vítimas da falta de proteção estatal e da objetificação extrema por parte dos agressores.',
  },
]

const handleScroll = () => {
  const height = document.documentElement.scrollHeight - document.documentElement.clientHeight
  scrollProgress.value = (window.scrollY / height) * 100
}

onMounted(() => window.addEventListener('scroll', handleScroll))
onUnmounted(() => window.removeEventListener('scroll', handleScroll))
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,500;0,700;1,400&family=Inter:wght@300;400;500;600&display=swap');

:root {
  --nude-light: #fdfaf7;
  --nude-mid: #f3e9dc;
  --sand: #d9c5b2;
  --clay: #a67c52;
  --brown: #4a3728;
  --skin-dark: #2d241e;
  --accent: #8c5a44;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 0;
  background-color: var(--nude-light);
  color: var(--skin-dark);
  font-family: 'Inter', sans-serif;
  line-height: 1.7;
  overflow-x: hidden;
}

.content-limit {
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 24px;
}

.reading-progress {
  position: fixed;
  top: 0;
  height: 4px;
  background: var(--accent);
  z-index: 1000;
  transition: width 0.1s;
}

/* Header */
.editorial-header {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  background: radial-gradient(circle at 50% 50%, var(--nude-mid) 0%, var(--nude-light) 100%);
  padding: 40px 20px;
}

.tag-line {
  text-transform: uppercase;
  letter-spacing: 0.2em;
  font-size: 0.7rem;
  font-weight: 600;
  color: var(--clay);
  margin-bottom: 20px;
}

.main-title {
  font-family: 'Playfair Display', serif;
  font-size: clamp(2.5rem, 10vw, 5rem);
  line-height: 1.1;
  color: var(--brown);
  margin: 0;
}

.main-title .italic {
  font-style: italic;
  font-weight: 400;
}

.abstract {
  max-width: 550px;
  margin: 30px auto;
  font-size: clamp(1rem, 3vw, 1.15rem);
  font-weight: 300;
  color: var(--skin-dark);
  opacity: 0.8;
}

.scroll-indicator {
  margin-top: 40px;
  font-size: 1.5rem;
  animation: bounce 2s infinite;
  color: var(--clay);
}

Chapters
.chapter {
  padding: clamp(40px, 10vw, 80px) 0;
}

.chapter-info {
  display: flex;
  align-items: baseline;
  gap: 15px;
  margin-bottom: 30px;
}

.chapter-number {
  font-family: 'Playfair Display', serif;
  font-size: clamp(2rem, 5vw, 3rem);
  color: var(--sand);
}

.chapter-title {
  font-family: 'Playfair Display', serif;
  font-size: clamp(1.5rem, 4vw, 2.2rem);
  color: var(--brown);
}

.two-columns {
  display: grid;
  grid-template-columns: 1.4fr 1fr;
  gap: clamp(30px, 5vw, 60px);
  align-items: center;
}

.insight-box {
  background: var(--nude-mid);
  padding: clamp(24px, 5vw, 40px);
  border-radius: 60px 0 60px 0;
  font-family: 'Playfair Display', serif;
  font-style: italic;
  font-size: clamp(1.1rem, 3vw, 1.3rem);
  color: var(--clay);
  line-height: 1.4;
}

.insight-box.secondary {
  border-radius: 0 60px 0 60px;
  background: var(--sand);
  color: var(--brown);
}

/* Theory Grid */
.section-intro {
  margin-bottom: 40px;
}

.sub-title {
  font-family: 'Playfair Display', serif;
  font-size: clamp(1.4rem, 4vw, 1.8rem);
  margin: 0;
}

.theory-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 24px;
}

.theory-card {
  background: white;
  padding: clamp(24px, 4vw, 40px);
  border-radius: 32px;
  border: 1px solid var(--nude-mid);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.02);
  transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
  display: flex;
  flex-direction: column;
  flex: 0 0 calc(50% - 12px);
}

.theory-card.full-width {
  width: 100%;
  flex: none;
  background: var(--nude-mid);
  border: 1px solid var(--sand);
}

.theory-card.full-width .card-content {
  max-width: 800px;
}

.theory-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 40px rgba(74, 55, 40, 0.1);
  border-color: var(--sand);
}

.card-head {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 18px;
}

.card-dot {
  width: 10px;
  height: 10px;
  background: var(--accent);
  border-radius: 50%;
  flex-shrink: 0;
}

.theory-card h3 {
  margin: 0;
  font-size: clamp(1rem, 2vw, 1.25rem);
  text-transform: uppercase;
  letter-spacing: 1.5px;
  color: var(--brown);
  font-weight: 600;
}

.theory-card p {
  margin: 0;
  font-size: clamp(0.95rem, 2vw, 1.05rem);
  color: var(--skin-dark);
  opacity: 0.9;
}

/* Accent Section Clay */
.accent-clay {
  background: var(--brown);
  color: var(--nude-mid);
  padding: clamp(60px, 10vw, 100px) clamp(24px, 5vw, 60px);
  border-radius: clamp(30px, 8vw, 80px);
  margin: 40px 0;
}

.quote-massive blockquote {
  font-family: 'Playfair Display', serif;
  font-size: clamp(1.4rem, 4vw, 2.2rem);
  text-align: center;
  border: none;
  margin: 0 0 clamp(30px, 6vw, 60px) 0;
  line-height: 1.3;
}

.reflexion-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: clamp(30px, 5vw, 50px);
}

.reflexion-item h4 {
  color: var(--sand);
  font-size: clamp(1.1rem, 3vw, 1.3rem);
  margin-bottom: 15px;
  font-family: 'Playfair Display', serif;
}

/* Data Container */
.data-container {
  background: white;
  padding: clamp(30px, 6vw, 60px);
  border-radius: clamp(30px, 5vw, 50px);
  box-shadow: 0 20px 50px rgba(74, 55, 40, 0.08);
}

.data-header {
  text-align: center;
  margin-bottom: clamp(30px, 5vw, 50px);
}

.year-tag {
  font-size: 0.9rem;
  background: var(--nude-mid);
  padding: 4px 12px;
  border-radius: 20px;
  vertical-align: middle;
}

.stats-row {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  gap: 30px;
}

.stat-circle {
  text-align: center;
  width: 100%;
  max-width: 220px;
}

.stat-num {
  display: block;
  font-family: 'Playfair Display', serif;
  font-size: clamp(2.5rem, 5vw, 3rem);
  color: var(--accent);
  line-height: 1;
  margin-bottom: 10px;
}

.stat-label {
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--clay);
  line-height: 1.4;
}

/* Footer */
.main-footer {
  background: var(--nude-mid);
  padding: clamp(40px, 8vw, 80px) 0 40px;
  margin-top: 60px;
}

.footer-grid {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: clamp(40px, 10vw, 100px);
  padding-bottom: 40px;
}

.footer-brand h3 {
  font-family: 'Playfair Display', serif;
  margin-top: 0;
  font-size: clamp(1.4rem, 4vw, 1.8rem);
}

.footer-source .label {
  font-size: 0.7rem;
  font-weight: 800;
  text-transform: uppercase;
  color: var(--clay);
  margin-bottom: 10px;
  display: block;
}

.footer-copyright {
  padding-top: 30px;
  font-size: 0.75rem;
  opacity: 0.6;
}

.data-note {
  font-size: 0.75rem;
  opacity: 0.6;
  margin-top: 10px;
}

@keyframes bounce {
  0%,
  20%,
  50%,
  80%,
  100% {
    transform: translateY(0);
  }

  40% {
    transform: translateY(-10px);
  }

  60% {
    transform: translateY(-5px);
  }
}

/* Responsividade Global */
@media (max-width: 900px) {
  .two-columns {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .insight-box {
    order: -1;
  }

  .footer-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }
}

@media (max-width: 768px) {
  .theory-card {
    flex: 0 0 100%;
  }

  .reflexion-grid {
    grid-template-columns: 1fr;
    gap: 30px;
  }
}

@media (max-width: 480px) {
  .tag-line {
    font-size: 0.8rem;
    padding-bottom: 5vw;
  }
  .main-title {
    font-size: 2.5  rem;
    line-height: 15vw;
    padding-bottom: 8vw;
  }
  .editorial-header {
    padding-inline: 20px;
    min-height: fit-content;
    padding-top: 30vw;
    padding-bottom: 20vw;
  }
  .abstract {
    line-height: 10vw;
    font-size: clamp(1.2rem, 3vw, 1.15rem);
    padding-inline: 0.5rem;
  }
  .content-limit {
    padding: 0 20px;
  }

  .chapter-info {
    flex-direction: column;
    gap: 5px;
  }
}
</style>
