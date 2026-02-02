# Diretrizes de Design - Estilo Racing / Motorsport

## Visão Geral

Design cinematográfico, high-tech e de alta performance inspirado em Fórmula 1 e motorsport. Tema escuro com acentos vibrantes em laranja e ciano. Transmite velocidade, precisão, tecnologia de ponta e adrenalina. Estilo "cinematic racing" com fotografia dramática.

---

## Paleta de Cores

### Cores Primárias

| Cor | Hex | Uso |
|-----|-----|-----|
| Preto Profundo | `#000000` | Background principal |
| Preto Suave | `#0a0a0a` | Seções alternadas |
| Cinza Escuro | `#111111` | Cards, containers |
| Laranja Racing | `#ff6b00` | Acentos principais, CTAs |
| Laranja McLaren | `#ff8000` | Highlights, hovers |

### Cores de Acento

| Cor | Hex | Uso |
|-----|-----|-----|
| Ciano Elétrico | `#00e5ff` | Links, títulos destacados |
| Azul Tech | `#0099ff` | Elementos secundários |
| Amarelo Neon | `#d4ff00` | Alertas, badges especiais |
| Verde Neon | `#39ff14` | Status, indicadores |

### Cores de Texto

| Cor | Hex | Uso |
|-----|-----|-----|
| Branco Puro | `#ffffff` | Títulos principais |
| Cinza Claro | `#e0e0e0` | Texto corpo |
| Cinza Médio | `#808080` | Labels, texto auxiliar |
| Cinza Escuro | `#404040` | Texto desabilitado |

### Gradientes

```css
/* Gradiente Laranja Racing */
background: linear-gradient(135deg, #ff6b00 0%, #ff8c00 50%, #ffa500 100%);

/* Gradiente Ciano Tech */
background: linear-gradient(90deg, #00e5ff 0%, #0099ff 100%);

/* Gradiente Escuro Dramático */
background: linear-gradient(180deg, #000000 0%, #0a0a0a 50%, #111111 100%);

/* Overlay para imagens */
background: linear-gradient(180deg,
  rgba(0,0,0,0) 0%,
  rgba(0,0,0,0.3) 50%,
  rgba(0,0,0,0.95) 100%
);
```

---

## Tipografia

### Famílias de Fontes

```css
/* Títulos - Condensada, Bold, Futurista */
font-family: 'Bebas Neue', 'Oswald', 'Impact', sans-serif;

/* Alternativa moderna */
font-family: 'Rajdhani', 'Exo 2', 'Orbitron', sans-serif;

/* Corpo - Clean, Legível */
font-family: 'Inter', 'Roboto', 'Arial', sans-serif;

/* Monospace - Dados técnicos */
font-family: 'JetBrains Mono', 'Fira Code', monospace;
```

### Hierarquia Tipográfica

| Elemento | Tamanho | Peso | Estilo |
|----------|---------|------|--------|
| H1 (Hero) | 80px - 120px | 700-900 | Uppercase, condensed |
| H2 (Seção) | 48px - 64px | 700 | Uppercase |
| H3 (Subtítulo) | 32px - 40px | 600 | Normal ou uppercase |
| Tagline | 18px - 24px | 400 | Italic, letter-spacing |
| Corpo | 16px | 400 | Line-height: 1.6 |
| Label | 12px - 14px | 500 | Uppercase, monospace |
| Dados Técnicos | 14px | 400 | Monospace |
| CTA | 14px - 16px | 700 | Uppercase, tracking wide |

### Características Especiais

```css
/* Título estilo corrida */
.racing-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 100px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  line-height: 0.9;
}

/* Tagline cinematográfica */
.tagline {
  font-family: 'Inter', sans-serif;
  font-size: 20px;
  font-weight: 300;
  font-style: italic;
  letter-spacing: 0.2em;
  color: #808080;
}

/* Dados técnicos */
.tech-data {
  font-family: 'JetBrains Mono', monospace;
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: #00e5ff;
}
```

---

## Layout

### Estrutura da Página

```
┌─────────────────────────────────────────────────────────┐
│  HEADER (fixo, transparente → sólido no scroll)         │
│  [Logo] ─────────────── [Nav] [Nav] [Nav] ─── [CTA]    │
├─────────────────────────────────────────────────────────┤
│                                                         │
│              HERO SECTION (100vh)                       │
│         ┌─────────────────────────────────┐            │
│         │   IMAGEM FULL-BLEED             │            │
│         │   (carro em movimento)          │            │
│         │                                 │            │
│         │   ┌─────────────────────┐       │            │
│         │   │ TÍTULO BOLD         │       │            │
│         │   │ Tagline             │       │            │
│         │   │ [CTA]               │       │            │
│         │   └─────────────────────┘       │            │
│         └─────────────────────────────────┘            │
│                                                         │
├─────────────────────────────────────────────────────────┤
│  SEÇÃO SPECS / FEATURES                                 │
│  ┌──────────┬──────────┬──────────┬──────────┐         │
│  │  STAT    │  STAT    │  STAT    │  STAT    │         │
│  │  Número  │  Número  │  Número  │  Número  │         │
│  │  Label   │  Label   │  Label   │  Label   │         │
│  └──────────┴──────────┴──────────┴──────────┘         │
├─────────────────────────────────────────────────────────┤
│  GALERIA CINEMATOGRÁFICA                                │
│  ┌─────────────────────────────────────────────┐       │
│  │  IMAGEM PRINCIPAL WIDE                      │       │
│  └─────────────────────────────────────────────┘       │
│  ┌─────────────┬─────────────┬─────────────────┐       │
│  │   THUMB     │    THUMB    │     THUMB       │       │
│  └─────────────┴─────────────┴─────────────────┘       │
├─────────────────────────────────────────────────────────┤
│  SEÇÃO VIDEO/PLAYER                                     │
│  ┌─────────────────────────────────────────────┐       │
│  │  ▶  VIDEO PLAYER                            │       │
│  │     Controles minimalistas                  │       │
│  └─────────────────────────────────────────────┘       │
├─────────────────────────────────────────────────────────┤
│  SEÇÃO TEXTO + IMAGEM (Bento Grid)                     │
│  ┌───────────────────┬─────────────────────────┐       │
│  │  Título           │                         │       │
│  │  Texto            │    IMAGEM               │       │
│  │  [CTA]            │                         │       │
│  └───────────────────┴─────────────────────────┘       │
└─────────────────────────────────────────────────────────┘
```

### Grid System

```css
/* Container principal */
.container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 48px;
}

/* Grid de stats */
.stats-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 2px;
  background: #1a1a1a;
}

/* Grid de galeria */
.gallery-grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 4px;
}

/* Bento grid */
.bento-grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 24px;
}
```

### Espaçamentos

| Elemento | Valor |
|----------|-------|
| Seções padding | 120px - 160px vertical |
| Gap galeria | 2px - 4px (tight) |
| Gap cards | 24px |
| Margem títulos | 48px bottom |
| Padding interno | 48px - 64px |

---

## Componentes

### Header Navigation

```css
.header {
  position: fixed;
  top: 0;
  width: 100%;
  padding: 24px 48px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: transparent;
  transition: background 0.3s ease;
  z-index: 1000;
}

.header.scrolled {
  background: rgba(0, 0, 0, 0.95);
  backdrop-filter: blur(10px);
}

.nav-link {
  font-family: 'Inter', sans-serif;
  font-size: 12px;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 0.15em;
  color: #808080;
  text-decoration: none;
  padding: 8px 0;
  position: relative;
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: #ffffff;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 1px;
  background: #ff6b00;
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}

.nav-link.active {
  color: #ff6b00;
}
```

### Botão CTA Racing

```css
.btn-racing {
  background: #ff6b00;
  border: none;
  padding: 16px 32px;
  font-family: 'Inter', sans-serif;
  font-size: 12px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.15em;
  color: #000000;
  cursor: pointer;
  position: relative;
  overflow: hidden;
  transition: all 0.3s ease;
}

.btn-racing::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
  transition: left 0.5s ease;
}

.btn-racing:hover::before {
  left: 100%;
}

.btn-racing:hover {
  background: #ff8000;
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(255, 107, 0, 0.4);
}
```

### Botão Outline

```css
.btn-outline {
  background: transparent;
  border: 1px solid #ffffff;
  padding: 16px 32px;
  font-size: 12px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.15em;
  color: #ffffff;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn-outline:hover {
  background: #ffffff;
  color: #000000;
}
```

### Card de Estatística

```css
.stat-card {
  background: #0a0a0a;
  padding: 48px 32px;
  text-align: center;
  border: 1px solid #1a1a1a;
  transition: all 0.3s ease;
}

.stat-card:hover {
  background: #111111;
  border-color: #ff6b00;
}

.stat-number {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 64px;
  font-weight: 700;
  color: #ffffff;
  line-height: 1;
  margin-bottom: 8px;
}

.stat-number span {
  color: #ff6b00;
}

.stat-label {
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.2em;
  color: #808080;
}
```

### Card de Imagem/Galeria

```css
.gallery-item {
  position: relative;
  overflow: hidden;
  cursor: pointer;
}

.gallery-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.6s ease;
}

.gallery-item:hover img {
  transform: scale(1.05);
}

.gallery-item__overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(180deg, transparent 50%, rgba(0,0,0,0.8) 100%);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.gallery-item:hover .gallery-item__overlay {
  opacity: 1;
}

.gallery-item__caption {
  position: absolute;
  bottom: 24px;
  left: 24px;
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: #ffffff;
  transform: translateY(20px);
  opacity: 0;
  transition: all 0.3s ease 0.1s;
}

.gallery-item:hover .gallery-item__caption {
  transform: translateY(0);
  opacity: 1;
}
```

### Video Player

```css
.video-container {
  position: relative;
  width: 100%;
  aspect-ratio: 16/9;
  background: #000000;
  overflow: hidden;
}

.video-controls {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 24px;
  background: linear-gradient(transparent, rgba(0,0,0,0.9));
  display: flex;
  align-items: center;
  gap: 16px;
}

.video-progress {
  flex: 1;
  height: 2px;
  background: #333333;
  cursor: pointer;
}

.video-progress__fill {
  height: 100%;
  background: #ff6b00;
  width: 0%;
  transition: width 0.1s linear;
}

.video-time {
  font-family: 'JetBrains Mono', monospace;
  font-size: 12px;
  color: #808080;
}
```

### Badge/Tag

```css
.badge {
  display: inline-block;
  padding: 6px 12px;
  font-family: 'JetBrains Mono', monospace;
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  background: #1a1a1a;
  color: #00e5ff;
  border: 1px solid #00e5ff;
}

.badge--orange {
  color: #ff6b00;
  border-color: #ff6b00;
}

.badge--filled {
  background: #ff6b00;
  color: #000000;
  border: none;
}
```

### Seção de Texto

```css
.text-section {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: center;
}

.text-section__label {
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.2em;
  color: #ff6b00;
  margin-bottom: 16px;
}

.text-section__title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 56px;
  text-transform: uppercase;
  line-height: 1;
  margin-bottom: 24px;
}

.text-section__body {
  font-size: 16px;
  color: #b0b0b0;
  line-height: 1.8;
  margin-bottom: 32px;
}
```

---

## Efeitos Visuais

### Motion Blur (para imagens)

```css
/* Simular motion blur com CSS */
.motion-blur {
  filter: blur(0);
  transition: filter 0.3s ease;
}

.motion-blur:hover {
  filter: blur(2px);
  transform: scale(1.02);
}

/* Overlay de velocidade */
.speed-lines {
  position: absolute;
  inset: 0;
  background: repeating-linear-gradient(
    90deg,
    transparent,
    transparent 10px,
    rgba(255,255,255,0.03) 10px,
    rgba(255,255,255,0.03) 11px
  );
  pointer-events: none;
}
```

### Glow Effects

```css
/* Glow laranja */
.glow-orange {
  box-shadow: 0 0 40px rgba(255, 107, 0, 0.3);
}

/* Glow ciano */
.glow-cyan {
  box-shadow: 0 0 40px rgba(0, 229, 255, 0.3);
}

/* Text glow */
.text-glow {
  text-shadow: 0 0 20px rgba(255, 107, 0, 0.5);
}
```

### Scanlines (Estilo TV)

```css
.scanlines::after {
  content: '';
  position: absolute;
  inset: 0;
  background: repeating-linear-gradient(
    0deg,
    transparent,
    transparent 2px,
    rgba(0, 0, 0, 0.1) 2px,
    rgba(0, 0, 0, 0.1) 4px
  );
  pointer-events: none;
}
```

### Noise Texture

```css
.noise-overlay {
  position: relative;
}

.noise-overlay::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)'/%3E%3C/svg%3E");
  opacity: 0.03;
  pointer-events: none;
}
```

### Animações

```css
/* Fade up on scroll */
@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Pulse para elementos live */
@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.5; }
}

/* Slide in horizontal */
@keyframes slideIn {
  from {
    opacity: 0;
    transform: translateX(-30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

/* Contador numérico */
@keyframes countUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate-on-scroll {
  opacity: 0;
  animation: fadeUp 0.8s ease forwards;
}
```

---

## Imagens e Fotografia

### Estilo de Fotografia

| Aspecto | Diretriz |
|---------|----------|
| **Iluminação** | Dramática, baixa luz, highlights fortes |
| **Ângulos** | Dinâmicos, perspectiva de velocidade |
| **Cores** | Alto contraste, cores vibrantes em fundo escuro |
| **Movimento** | Motion blur, senso de velocidade |
| **Detalhes** | Close-ups mecânicos, texturas metálicas |

### Tratamento de Imagem

```css
/* Filtro cinematográfico */
.cinematic-filter {
  filter: contrast(1.1) saturate(1.2);
}

/* High contrast racing */
.high-contrast {
  filter: contrast(1.2) brightness(0.95);
}

/* Teal & Orange (cinema look) */
.teal-orange {
  filter: sepia(0.1) saturate(1.3) hue-rotate(-10deg);
}
```

### Tipos de Imagem

1. **Hero shots**: Full-bleed, carro em movimento
2. **Detail shots**: Close-ups de peças, texturas
3. **Ambient shots**: Pit lane, paddock, ambiente
4. **Action shots**: Momentos dinâmicos, velocidade
5. **Portrait shots**: Pilotos, equipe (iluminação dramática)

---

## Elementos de Conversão

### Headline Impactante

```html
<div class="hero-headline">
  <span class="label">HALO × McLaren F1</span>
  <h1>CHANGE THE WAY<br>THE WORLD <span>WORKS</span></h1>
  <p class="tagline">Las Vegas 2025</p>
</div>
```

```css
.hero-headline h1 span {
  color: #00e5ff;
}
```

### Contador de Stats

```html
<div class="stats-bar">
  <div class="stat">
    <span class="stat__number">350+</span>
    <span class="stat__label">KM/H Top Speed</span>
  </div>
  <div class="stat">
    <span class="stat__number">1000</span>
    <span class="stat__label">Horsepower</span>
  </div>
  <div class="stat">
    <span class="stat__number">2.6</span>
    <span class="stat__label">0-100 Seconds</span>
  </div>
</div>
```

### Live Indicator

```css
.live-indicator {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.1em;
}

.live-indicator__dot {
  width: 8px;
  height: 8px;
  background: #ff3333;
  border-radius: 50%;
  animation: pulse 1.5s ease infinite;
}
```

---

## Responsividade

### Breakpoints

| Dispositivo | Largura |
|-------------|---------|
| Mobile | < 768px |
| Tablet | 768px - 1024px |
| Desktop | 1024px - 1400px |
| Wide | > 1400px |

### Adaptações Mobile

```css
@media (max-width: 768px) {
  .hero h1 {
    font-size: 48px;
  }

  .stats-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .gallery-grid {
    grid-template-columns: 1fr;
  }

  .text-section {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .container {
    padding: 0 24px;
  }

  .nav-links {
    display: none; /* Menu hamburguer */
  }

  .stat-number {
    font-size: 48px;
  }
}
```

---

## Exemplo de Implementação

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HALO × McLaren F1</title>
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Inter:wght@300;400;500;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #000000;
      color: #ffffff;
      overflow-x: hidden;
    }

    /* Header */
    .header {
      position: fixed;
      top: 0;
      width: 100%;
      padding: 24px 48px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      z-index: 1000;
      background: transparent;
      transition: background 0.3s ease;
    }

    .header.scrolled {
      background: rgba(0, 0, 0, 0.95);
    }

    .logo {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 24px;
      letter-spacing: 0.1em;
    }

    .nav {
      display: flex;
      gap: 48px;
    }

    .nav a {
      font-size: 11px;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: 0.15em;
      color: #808080;
      text-decoration: none;
      transition: color 0.3s ease;
    }

    .nav a:hover {
      color: #ffffff;
    }

    /* Hero */
    .hero {
      min-height: 100vh;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .hero-bg {
      position: absolute;
      inset: 0;
      background: url('hero-f1.jpg') center/cover;
    }

    .hero-overlay {
      position: absolute;
      inset: 0;
      background: linear-gradient(180deg,
        rgba(0,0,0,0.3) 0%,
        rgba(0,0,0,0.5) 50%,
        rgba(0,0,0,0.95) 100%
      );
    }

    .hero-content {
      position: relative;
      text-align: center;
      z-index: 1;
    }

    .hero-label {
      font-family: 'JetBrains Mono', monospace;
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.3em;
      color: #ff6b00;
      margin-bottom: 24px;
    }

    .hero h1 {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 120px;
      text-transform: uppercase;
      line-height: 0.9;
      margin-bottom: 24px;
    }

    .hero h1 span {
      color: #00e5ff;
    }

    .hero-tagline {
      font-size: 18px;
      font-weight: 300;
      font-style: italic;
      letter-spacing: 0.2em;
      color: #808080;
      margin-bottom: 48px;
    }

    .btn-racing {
      background: #ff6b00;
      border: none;
      padding: 18px 40px;
      font-family: 'Inter', sans-serif;
      font-size: 12px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.15em;
      color: #000000;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .btn-racing:hover {
      background: #ff8000;
      transform: translateY(-2px);
      box-shadow: 0 8px 24px rgba(255, 107, 0, 0.4);
    }

    /* Stats */
    .stats {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      border-top: 1px solid #1a1a1a;
      border-bottom: 1px solid #1a1a1a;
    }

    .stat {
      padding: 48px 32px;
      text-align: center;
      border-right: 1px solid #1a1a1a;
    }

    .stat:last-child {
      border-right: none;
    }

    .stat__number {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 56px;
      color: #ffffff;
      line-height: 1;
    }

    .stat__number span {
      color: #ff6b00;
    }

    .stat__label {
      font-family: 'JetBrains Mono', monospace;
      font-size: 10px;
      text-transform: uppercase;
      letter-spacing: 0.2em;
      color: #808080;
      margin-top: 8px;
    }

    /* Gallery */
    .gallery {
      padding: 120px 48px;
    }

    .gallery-label {
      font-family: 'JetBrains Mono', monospace;
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.2em;
      color: #808080;
      margin-bottom: 32px;
    }

    .gallery-grid {
      display: grid;
      grid-template-columns: 2fr 1fr;
      grid-template-rows: 1fr 1fr;
      gap: 4px;
      height: 600px;
    }

    .gallery-item {
      position: relative;
      overflow: hidden;
    }

    .gallery-item:first-child {
      grid-row: span 2;
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.6s ease;
    }

    .gallery-item:hover img {
      transform: scale(1.05);
    }

    /* Brand Section */
    .brand {
      padding: 160px 48px;
      text-align: center;
      background: #0a0a0a;
    }

    .brand h2 {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 80px;
      color: #00e5ff;
      margin-bottom: 24px;
    }

    .brand p {
      font-size: 20px;
      font-weight: 300;
      font-style: italic;
      color: #808080;
    }

    /* Footer */
    .footer {
      padding: 48px;
      text-align: center;
      border-top: 1px solid #1a1a1a;
    }

    .footer p {
      font-size: 12px;
      color: #404040;
      letter-spacing: 0.1em;
    }
  </style>
</head>
<body>
  <header class="header">
    <div class="logo">HALO</div>
    <nav class="nav">
      <a href="#">Project</a>
      <a href="#">Services</a>
      <a href="#">Project Brief</a>
    </nav>
  </header>

  <section class="hero">
    <div class="hero-bg"></div>
    <div class="hero-overlay"></div>
    <div class="hero-content">
      <p class="hero-label">HALO × McLaren F1 — Las Vegas 2025</p>
      <h1>CHANGE THE WAY<br>THE WORLD <span>WORKS</span></h1>
      <p class="hero-tagline">Creative Direction & Motion Graphics</p>
      <button class="btn-racing">Watch Film</button>
    </div>
  </section>

  <section class="stats">
    <div class="stat">
      <div class="stat__number">350<span>+</span></div>
      <div class="stat__label">KM/H Top Speed</div>
    </div>
    <div class="stat">
      <div class="stat__number">1000</div>
      <div class="stat__label">Horsepower</div>
    </div>
    <div class="stat">
      <div class="stat__number">2.6<span>s</span></div>
      <div class="stat__label">0-100 KM/H</div>
    </div>
    <div class="stat">
      <div class="stat__number">24</div>
      <div class="stat__label">Races</div>
    </div>
  </section>

  <section class="gallery">
    <p class="gallery-label">Still Frames</p>
    <div class="gallery-grid">
      <div class="gallery-item">
        <img src="gallery-1.jpg" alt="F1 Car">
      </div>
      <div class="gallery-item">
        <img src="gallery-2.jpg" alt="Detail">
      </div>
      <div class="gallery-item">
        <img src="gallery-3.jpg" alt="Action">
      </div>
    </div>
  </section>

  <section class="brand">
    <h2>HALO</h2>
    <p>Change the way the world works.</p>
  </section>

  <footer class="footer">
    <p>© 2025 HALO × McLaren F1</p>
  </footer>

  <script>
    // Header scroll effect
    window.addEventListener('scroll', () => {
      const header = document.querySelector('.header');
      if (window.scrollY > 100) {
        header.classList.add('scrolled');
      } else {
        header.classList.remove('scrolled');
      }
    });
  </script>
</body>
</html>
```

---

## Checklist de Implementação

- [ ] Background preto puro (#000000)
- [ ] Tipografia condensada bold (Bebas Neue)
- [ ] Cores de acento: laranja (#ff6b00) e ciano (#00e5ff)
- [ ] Header fixo com transição no scroll
- [ ] Hero full-bleed com overlay
- [ ] Stats com fonte monospace para labels
- [ ] Galeria com grid assimétrico
- [ ] Hover effects com scale nas imagens
- [ ] Botões com glow e hover states
- [ ] Animações sutis (fade up, slide)
- [ ] Espaçamentos generosos entre seções
- [ ] Responsividade completa
- [ ] Efeito noise/grain opcional
- [ ] Tratamento de imagem cinematográfico

---

## Resumo do Estilo

| Aspecto | Característica |
|---------|----------------|
| **Mood** | Velocidade, High-tech, Premium, Adrenalina |
| **Tema** | Ultra Dark (#000000) |
| **Cores** | Laranja Racing + Ciano Tech |
| **Tipografia** | Bebas Neue (condensed), JetBrains Mono (dados) |
| **Imagens** | Cinematográficas, motion blur, dramáticas |
| **Layout** | Full-bleed, grid assimétrico, espaçamento tight |
| **Efeitos** | Glow, hover scale, scroll animations |
| **Conversão** | Stats numéricas, CTAs vibrantes |
