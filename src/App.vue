<template>
  <div id="app">
    <div class="progress-bar" :style="{ width: scrollProgress + '%' }"></div>

    <header class="hero">
      <div class="container">
        <p class="tagline">Perspectivas em Saúde Mental e Gênero</p>
        <h1 class="hero-title">A Gramática da <br><span>Masculinidade</span></h1>
        <p class="hero-subtitle">
          Uma análise sobre as engrenagens de poder, o dividendo patriarcal e as
          consequências da hegemonia na saúde mental dos homens.
        </p>
        <div class="scroll-indicator">↓</div>
      </div>
    </header>

    <main class="container">
      <section class="section">
        <div class="chapter-header">
          <span class="chapter-number">01</span>
          <h2 class="chapter-title">Hegemonia e o Jogo Social</h2>
        </div>

        <div class="grid-two-cols">
          <div class="content-text">
            <p class="mb-20">
              A <strong>masculinidade hegemônica</strong> (Connell, 2005) não é um estado natural, mas um jogo de poder complexo.
              Ela estabelece performances "honradas" que garantem liderança e autoridade, subordinando não apenas mulheres,
              mas outras formas de masculinidade.
            </p>
            <p>
              Muitos homens sustentam as bases da sociedade de forma invisível, muitas vezes gratificados por pequenos benefícios
              do sistema (o dividendo patriarcal), enquanto lidam com a pressão silenciosa de nunca poderem falhar ou demonstrar vulnerabilidade.
            </p>
          </div>
          <div class="quote-box">
            "A hegemonia pressupõe a predominância de uma certa configuração de feminilidade. É um jogo social permeado de poder."
          </div>
        </div>
      </section>

      <section class="theory-container">
        <div class="theory-header">
          <h2>As Quatro Relações de Connell</h2>
          <p>O funcionamento interno e externo da ordem de gênero</p>
        </div>

        <div class="theory-grid">
          <div v-for="t in teoria" :key="t.name" class="card">
            <div class="card-title">
              <span class="dot"></span>
              {{ t.name }}
            </div>
            <p class="card-desc">{{ t.desc }}</p>
          </div>
        </div>
      </section>

      <section class="dark-banner">
        <div class="massive-quote">
          "O silêncio face à opressão é o que mantém o dividendo patriarcal, mesmo para quem não se enquadra no padrão."
        </div>
        <div class="banner-flex">
          <div class="banner-item">
            <h4>Cumplicidade e Silêncio</h4>
            <p>
              Realiza-se pelo silêncio diante de piadas ou assédios. Esse silêncio baseia-se no medo de ser desvalorizado pelos pares,
              criando uma barreira que impede conexões emocionais reais entre os homens.
            </p>
          </div>
          <div class="banner-item">
            <h4>Marginalização Institucional</h4>
            <p>
              A interseccionalidade com raça e classe. Homens negros e pobres são marginalizados pelo Estado,
              vistos como "perigosos" ou "sem razão", o que gera um sofrimento mental profundo e específico.
            </p>
          </div>
        </div>
      </section>

      <section class="section">
        <div class="chapter-header">
          <span class="chapter-number">02</span>
          <h2 class="chapter-title">Saúde Mental e Resistência</h2>
        </div>
        <div class="grid-two-cols">
          <div class="quote-box quote-alt">
            "Tratar a agressividade exige acolher o sofrimento que a precede. A hegemonia pode fracassar."
          </div>
          <div class="content-text">
            <p class="mb-20">
              A busca pelo ideal hegemônico gera angústia. Quando o homem não atinge o sucesso ou o controle esperado,
              o "dispositivo de eficácia" entra em colapso, resultando em depressão ou reações agressivas defensivas.
            </p>
            <p>
              No entanto, há agência. Movimentos de resistência (posições rebeldes) buscam novas formas de existir
              que não dependam da dominação, abrindo caminho para uma saúde mental mais saudável e afetiva.
            </p>
          </div>
        </div>

        <div class="stats-card">
          <h3>Retrato da Violência Contra a Mulher 2023 / 2024</h3>
          <p class="stats-subtitle">O feminicídio representa a consequência mais extrema das desigualdades nas relações de gênero.</p>
          <div class="stats-row">
            <div v-for="stat in estatisticas" :key="stat.label" class="stat-item">
              <span class="stat-value">{{ stat.value }}</span>
              <span class="stat-label" v-html="stat.label"></span>
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer>
      <div class="container footer-grid">
        <div>
          <h3>Educação & Gênero</h3>
          <p>Pela construção de masculinidades que permitam o sentir e o cuidar.</p>
        </div>
        <div class="footer-source">
          <p><strong>Referência Bibliográfica Principal:</strong></p>
          <p>ZANELLO, Valeska. Saúde mental, gênero e dispositivos: cultura e processos de subjetivação. Curitiba: Appris, 2018. Pp. 228-229.</p>
          <p class="footer-subtext">Baseado em Connell (2005), Matos (2001) e Anuário de Segurança Pública.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

// Estado para a barra de progresso
const scrollProgress = ref(0);

// Dados da teoria
const teoria = [
  {
    name: 'Hegemonia',
    desc: 'Eleição de performances "honradas" que sustentam a liderança social e o poder sobre outras masculinidades.'
  },
  {
    name: 'Subordinação',
    desc: 'Processo de abuso e exclusão cultural de masculinidades que não seguem o padrão (ex: homens gays).'
  },
  {
    name: 'Cumplicidade',
    desc: 'O "dividendo patriarcal" usufruído por homens que silenciam perante a opressão para manter seu status.'
  },
  {
    name: 'Marginalização',
    desc: 'Relação externa baseada em raça e classe, onde sujeitos são vistos como perigosos ou desprovidos de razão.'
  }
];

// Dados das estatísticas
const estatisticas = [
  { value: '1.467', label: 'Mulheres assassinadas em 2023 <br>(Maior índice registrado)' },
  { value: '61,1%', label: 'Das vítimas de feminicídio <br>são mulheres negras' },
  { value: '1 a cada 6', label: 'Horas uma mulher é morta <br>por ser mulher no Brasil' }
];

// Lógica de Scroll
const updateScroll = () => {
  const totalHeight = document.documentElement.scrollHeight - document.documentElement.clientHeight;
  if (totalHeight > 0) {
    scrollProgress.value = (window.scrollY / totalHeight) * 100;
  }
};

onMounted(() => {
  window.addEventListener('scroll', updateScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', updateScroll);
});
</script>

<style scoped>
/* Importação de fontes (pode ser movido para o index.html ou main.js) */
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

#app {
  background-color: #fdfaf7; /* Fallback do var */
  color: #2d241e;
  font-family: 'Inter', sans-serif;
  line-height: 1.7;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

/* Utilitários */
.container { max-width: 1000px; margin: 0 auto; padding: 0 24px; }
.mb-20 { margin-bottom: 20px; }

/* Progress Bar */
.progress-bar {
  position: fixed;
  top: 0;
  left: 0;
  height: 4px;
  background: #8c5a44;
  z-index: 1000;
  transition: width 0.1s ease;
}

/* Hero */
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  background: radial-gradient(circle at 50% 50%, #f3e9dc 0%, #fdfaf7 100%);
  padding: 40px 20px;
}

.tagline {
  text-transform: uppercase;
  letter-spacing: 0.2em;
  font-size: 0.75rem;
  font-weight: 700;
  color: #a67c52;
  margin-bottom: 20px;
}

.hero-title {
  font-family: 'Playfair Display', serif;
  font-size: clamp(2.2rem, 8vw, 4.5rem);
  line-height: 1.1;
  color: #4a3728;
}

.hero-title span { font-style: italic; font-weight: 400; }

.hero-subtitle {
  max-width: 600px;
  margin: 30px auto;
  font-size: clamp(1rem, 3vw, 1.2rem);
  font-weight: 300;
  opacity: 0.9;
}

.scroll-indicator { margin-top: 40px; font-size: 1.5rem; color: #8c5a44; }

/* Sections */
.section { padding: 80px 0; }

.chapter-header {
  display: flex;
  align-items: baseline;
  gap: 15px;
  margin-bottom: 40px;
}

.chapter-number {
  font-family: 'Playfair Display', serif;
  font-size: 3rem;
  color: #d9c5b2;
}

.chapter-title {
  font-family: 'Playfair Display', serif;
  font-size: 2rem;
  color: #4a3728;
}

.grid-two-cols {
  display: grid;
  grid-template-columns: 1.4fr 1fr;
  gap: 50px;
  align-items: center;
}

.quote-box {
  background: #f3e9dc;
  padding: 40px;
  border-radius: 60px 0 60px 0;
  font-family: 'Playfair Display', serif;
  font-style: italic;
  font-size: 1.25rem;
  color: #a67c52;
  line-height: 1.4;
}

.quote-alt {
  border-radius: 0 60px 0 60px;
  background: #d9c5b2;
  color: #4a3728;
}

/* Theory Cards */
.theory-container {
  background-color: rgba(243, 233, 220, 0.3);
  border-radius: 40px;
  padding: 60px 30px;
  margin: 40px 0;
}

.theory-header { text-align: center; margin-bottom: 30px; }
.theory-header h2 { font-family: 'Playfair Display', serif; }
.theory-header p { opacity: 0.7; }

.theory-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 24px;
  margin-top: 40px;
}

.card {
  background: white;
  padding: 32px;
  border-radius: 24px;
  border: 1px solid #f3e9dc;
  transition: all 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(74, 55, 40, 0.1);
}

.card-title {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 15px;
  text-transform: uppercase;
  font-size: 0.85rem;
  font-weight: 600;
  color: #4a3728;
}

.dot { width: 8px; height: 8px; background: #8c5a44; border-radius: 50%; }
.card-desc { font-size: 0.95rem; opacity: 0.9; }

/* Dark Banner */
.dark-banner {
  background: #4a3728;
  color: #f3e9dc;
  padding: 80px 40px;
  border-radius: 60px;
  margin: 60px 0;
  text-align: center;
}

.massive-quote {
  font-family: 'Playfair Display', serif;
  font-size: clamp(1.4rem, 4vw, 2rem);
  margin: 0 auto 50px;
  max-width: 800px;
}

.banner-flex {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  text-align: left;
}

.banner-item h4 {
  color: #d9c5b2;
  font-family: 'Playfair Display', serif;
  font-size: 1.3rem;
  margin-bottom: 10px;
}

.banner-item p { opacity: 0.8; font-size: 0.95rem; }

/* Stats */
.stats-card {
  background: white;
  padding: 50px;
  border-radius: 40px;
  box-shadow: 0 20px 40px rgba(0,0,0,0.05);
  margin-top: 40px;
  text-align: center;
}

.stats-card h3 { font-family: 'Playfair Display', serif; margin-bottom: 5px; }
.stats-subtitle { opacity: 0.7; font-size: 0.9rem; margin-bottom: 30px; }

.stats-row {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  gap: 30px;
  margin-top: 40px;
}

.stat-item { flex: 1; min-width: 150px; }
.stat-value {
  display: block;
  font-family: 'Playfair Display', serif;
  font-size: 3rem;
  color: #8c5a44;
  margin-bottom: 5px;
}

.stat-label {
  font-size: 0.75rem;
  font-weight: 700;
  text-transform: uppercase;
  color: #a67c52;
}

/* Footer */
footer { background: #f3e9dc; padding: 60px 0; margin-top: auto; }

.footer-grid {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: 60px;
}

.footer-grid h3 { font-family: 'Playfair Display', serif; margin-bottom: 10px; }

.footer-source { font-size: 0.85rem; opacity: 0.8; }
.footer-source strong { display: block; margin-top: 10px; }
.footer-subtext { margin-top: 10px; font-size: 0.75rem; opacity: 0.6; }

/* Responsive */
@media (max-width: 850px) {
  .grid-two-cols, .banner-flex, .footer-grid { grid-template-columns: 1fr; }
  .hero-title { font-size: 2.5rem; }
}
</style>
