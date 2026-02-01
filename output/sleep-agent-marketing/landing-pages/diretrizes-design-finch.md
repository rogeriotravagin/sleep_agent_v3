# Diretrizes de Design - Página Thiago Finch (Nômade Milionário)

## Visão Geral

Design premium, tecnológico e aspiracional. Tema escuro com acentos em azul ciano. Transmite sucesso, liberdade financeira e lifestyle de alto padrão. Estilo "tech-luxury" com elementos futuristas.

---

## Paleta de Cores

### Cores Primárias

| Cor | Hex | Uso |
|-----|-----|-----|
| Azul Escuro (BG) | `#0a0e17` | Background principal |
| Azul Profundo | `#0d1520` | Cards, seções alternadas |
| Ciano Primário | `#00d4ff` | CTAs, destaques, acentos |
| Ciano Claro | `#4ae3ff` | Hover states, gradientes |

### Cores de Texto

| Cor | Hex | Uso |
|-----|-----|-----|
| Branco | `#ffffff` | Títulos, texto principal |
| Cinza Claro | `#b8c5d6` | Texto secundário, descrições |
| Cinza Médio | `#6b7a8f` | Labels, texto auxiliar |
| Azul Label | `#5ba3c0` | Labels "Pilar 1", categorias |

### Gradientes

```css
/* Gradiente CTA */
background: linear-gradient(90deg, #00b4d8 0%, #00d4ff 50%, #4ae3ff 100%);

/* Gradiente de fundo sutil */
background: radial-gradient(ellipse at 70% 30%, rgba(0, 212, 255, 0.15) 0%, transparent 50%);

/* Overlay para cards com imagem */
background: linear-gradient(180deg, rgba(10, 14, 23, 0.3) 0%, rgba(10, 14, 23, 0.95) 100%);
```

---

## Tipografia

### Famílias de Fontes

```css
/* Títulos e corpo */
font-family: 'Montserrat', 'Inter', sans-serif;

/* Logo script (Nômade Milionário) */
font-family: 'Playlist Script', 'Pacifico', cursive;

/* Texto destaque em itálico */
font-family: 'Montserrat', sans-serif;
font-style: italic;
```

### Hierarquia Tipográfica

| Elemento | Tamanho | Peso | Estilo |
|----------|---------|------|--------|
| Logo "PROJETO" | 18px | 600 | Letter-spacing: 0.4em, uppercase |
| Logo Script | 48px | 400 | Cursiva, fluida |
| H1 (Hero) | 48px - 56px | 600 | Normal |
| H1 Destaque | 48px - 56px | 700 | Itálico, cor ciano |
| Subtítulo | 18px - 20px | 400 | Line-height: 1.6 |
| Label (Pilar) | 14px | 500 | Monospace ou sans-serif |
| Título Card | 28px - 32px | 700 | Normal |
| Descrição Card | 14px - 16px | 400 | Line-height: 1.5 |
| Botão CTA | 16px - 18px | 700 | Uppercase, letter-spacing: 0.1em |

### Características Especiais

- **Destaque numérico**: Números grandes em itálico + cor ciano
- **Primeira letra destacada**: Em títulos de cards, primeira letra em ciano
- **Labels**: Estilo monospace para "Pilar 1", "Pilar 2", etc.

---

## Layout

### Estrutura da Página

```
┌─────────────────────────────────────────────────────────┐
│  HERO SECTION (100vh)                                   │
│  ┌─────────────────────┬───────────────────────────┐   │
│  │ LOGO                │                           │   │
│  │ HEADLINE            │    IMAGEM PRINCIPAL       │   │
│  │ (texto esquerda)    │    + Notificações        │   │
│  │                     │    + Elementos 3D        │   │
│  │ SUBHEADLINE         │                           │   │
│  │                     │                           │   │
│  │ [    CTA BUTTON    ]│                           │   │
│  │                     │                           │   │
│  │ 👤👤👤 Prova Social │                           │   │
│  └─────────────────────┴───────────────────────────┘   │
├─────────────────────────────────────────────────────────┤
│  SEÇÃO PILARES                                          │
│  ┌─────────────────────┬───────────────────────────┐   │
│  │     CARD PILAR 1    │      CARD PILAR 2         │   │
│  │  [Imagem + Overlay] │   [Imagem + Overlay]      │   │
│  │  Label | Título     │   Label | Título          │   │
│  │  Descrição          │   Descrição               │   │
│  ├─────────────────────┼───────────────────────────┤   │
│  │     CARD PILAR 3    │      CARD PILAR 4         │   │
│  │  [Imagem + Overlay] │   [Imagem + Overlay]      │   │
│  │  Label | Título     │   Label | Título          │   │
│  │  Descrição          │   Descrição               │   │
│  └─────────────────────┴───────────────────────────┘   │
└─────────────────────────────────────────────────────────┘
```

### Grid

```css
/* Container principal */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 40px;
}

/* Grid de pilares */
.pilares-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
}

/* Hero split layout */
.hero {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  min-height: 100vh;
}
```

### Espaçamentos

| Elemento | Valor |
|----------|-------|
| Padding seções | 80px - 120px vertical |
| Gap entre cards | 24px |
| Margem headline-subheadline | 24px |
| Margem subheadline-CTA | 32px |
| Padding interno cards | 32px |

---

## Componentes

### Botão CTA Principal

```css
.btn-cta {
  background: linear-gradient(90deg, #00b4d8 0%, #00d4ff 100%);
  border: none;
  border-radius: 8px;
  padding: 20px 48px;
  color: #0a0e17;
  font-size: 16px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 12px;
  transition: all 0.3s ease;
  box-shadow: 0 4px 24px rgba(0, 212, 255, 0.3);
}

.btn-cta:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 32px rgba(0, 212, 255, 0.5);
}

.btn-cta .arrow {
  font-size: 20px;
  transition: transform 0.3s ease;
}

.btn-cta:hover .arrow {
  transform: translateX(4px);
}
```

### Card de Pilar

```css
.pilar-card {
  position: relative;
  border-radius: 12px;
  overflow: hidden;
  background: #0d1520;
  min-height: 300px;
}

.pilar-card__image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 60%;
  object-fit: cover;
}

.pilar-card__overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(180deg,
    rgba(10, 14, 23, 0.2) 0%,
    rgba(10, 14, 23, 0.98) 70%
  );
}

.pilar-card__content {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 32px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
  align-items: start;
}

.pilar-card__label {
  font-family: 'JetBrains Mono', monospace;
  font-size: 14px;
  color: #5ba3c0;
  margin-bottom: 8px;
}

.pilar-card__title {
  font-size: 28px;
  font-weight: 700;
  color: white;
  line-height: 1.2;
}

.pilar-card__title span {
  color: #00d4ff;
}

.pilar-card__description {
  font-size: 14px;
  color: #b8c5d6;
  line-height: 1.6;
  border-left: 1px solid rgba(255, 255, 255, 0.2);
  padding-left: 24px;
}
```

### Notificação Flutuante (Glassmorphism)

```css
.notification {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.15);
  border-radius: 12px;
  padding: 12px 20px;
  display: flex;
  align-items: center;
  gap: 12px;
  color: white;
  font-size: 14px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
}

.notification__icon {
  width: 36px;
  height: 36px;
  background: #00d4ff;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.notification__text strong {
  display: block;
  font-weight: 600;
}

.notification__text span {
  font-size: 12px;
  color: rgba(255, 255, 255, 0.7);
}

.notification__time {
  font-size: 12px;
  color: rgba(255, 255, 255, 0.5);
}
```

### Prova Social

```css
.social-proof {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-top: 24px;
}

.social-proof__avatars {
  display: flex;
}

.social-proof__avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  border: 2px solid #0a0e17;
  margin-left: -12px;
  object-fit: cover;
}

.social-proof__avatar:first-child {
  margin-left: 0;
}

.social-proof__text {
  font-size: 14px;
  color: #b8c5d6;
}

.social-proof__text strong {
  color: white;
}
```

### Logo Composto

```css
.logo {
  display: flex;
  align-items: center;
  gap: 16px;
}

.logo__projeto {
  font-size: 18px;
  font-weight: 600;
  letter-spacing: 0.4em;
  text-transform: uppercase;
  color: white;
}

.logo__nome {
  font-family: 'Playlist Script', cursive;
  font-size: 48px;
  color: white;
  line-height: 0.8;
}
```

---

## Efeitos Visuais

### Glow Effect (Luz Ambiente)

```css
/* Glow azul atrás da imagem principal */
.hero-glow {
  position: absolute;
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(0, 212, 255, 0.3) 0%, transparent 70%);
  filter: blur(60px);
  z-index: -1;
}
```

### Elementos 3D Flutuantes

```css
/* Animação de flutuação */
@keyframes float {
  0%, 100% { transform: translateY(0) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(5deg); }
}

.floating-element {
  animation: float 4s ease-in-out infinite;
}

.floating-element:nth-child(2) {
  animation-delay: -1s;
}

.floating-element:nth-child(3) {
  animation-delay: -2s;
}
```

### Gradiente de Texto

```css
.gradient-text {
  background: linear-gradient(90deg, #00d4ff 0%, #4ae3ff 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
```

---

## Imagens e Elementos Visuais

### Estilo de Fotografia

- **Temática**: Lifestyle de luxo, sucesso, liberdade
- **Exemplos**: Carros esportivos, relógios de luxo, viagens, pessoa elegante
- **Tratamento**: Tom frio (azulado), alto contraste, iluminação dramática
- **Iluminação**: Luz azul/ciano como acento, ambiente escuro

### Elementos Gráficos

- **Notificações**: Cards glass de "Venda aprovada!"
- **3D Elements**: Cartões, dinheiro, objetos flutuando
- **Ícones**: Minimalistas, linha fina ou preenchidos em ciano

---

## Elementos de Conversão

### Headline Persuasiva

```html
<h1>
  O método secreto que já movimentou mais de<br>
  <em class="highlight">1 bilhão em vendas online</em>
</h1>
```

```css
.highlight {
  color: #00d4ff;
  font-style: italic;
}
```

### Prova Social Numérica

- "+ de 7000 alunos espalhados pelo mundo"
- Avatares reais de alunos
- Números grandes e destacados

### Urgência/Escassez

- Contadores regressivos (se aplicável)
- Badges de "Vagas limitadas"
- Notificações de vendas em tempo real

---

## Responsividade

### Breakpoints

| Dispositivo | Largura |
|-------------|---------|
| Mobile | < 768px |
| Tablet | 768px - 1024px |
| Desktop | > 1024px |

### Adaptações Mobile

```css
@media (max-width: 768px) {
  .hero {
    grid-template-columns: 1fr;
    text-align: center;
    padding-top: 100px;
  }

  .hero h1 {
    font-size: 32px;
  }

  .pilares-grid {
    grid-template-columns: 1fr;
  }

  .pilar-card__content {
    grid-template-columns: 1fr;
  }

  .pilar-card__description {
    border-left: none;
    border-top: 1px solid rgba(255, 255, 255, 0.2);
    padding-left: 0;
    padding-top: 16px;
  }

  .btn-cta {
    width: 100%;
    justify-content: center;
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
  <title>Projeto Nômade Milionário</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,400;0,600;0,700;1,700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Montserrat', sans-serif;
      background: #0a0e17;
      color: white;
      overflow-x: hidden;
    }

    .hero {
      min-height: 100vh;
      display: grid;
      grid-template-columns: 1fr 1fr;
      align-items: center;
      padding: 40px;
      position: relative;
    }

    .hero::before {
      content: '';
      position: absolute;
      right: 20%;
      top: 30%;
      width: 500px;
      height: 500px;
      background: radial-gradient(circle, rgba(0, 212, 255, 0.2) 0%, transparent 70%);
      filter: blur(80px);
      z-index: 0;
    }

    .hero-content {
      z-index: 1;
      max-width: 600px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 16px;
      margin-bottom: 40px;
    }

    .logo-projeto {
      font-size: 16px;
      font-weight: 600;
      letter-spacing: 0.4em;
    }

    .logo-nome {
      font-size: 36px;
      font-style: italic;
    }

    h1 {
      font-size: 48px;
      font-weight: 600;
      line-height: 1.2;
      margin-bottom: 24px;
    }

    h1 em {
      color: #00d4ff;
      font-style: italic;
      font-weight: 700;
    }

    .subtitle {
      font-size: 18px;
      color: #b8c5d6;
      line-height: 1.6;
      margin-bottom: 32px;
    }

    .btn-cta {
      background: linear-gradient(90deg, #00b4d8, #00d4ff);
      border: none;
      border-radius: 8px;
      padding: 20px 48px;
      color: #0a0e17;
      font-size: 16px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.1em;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 12px;
      box-shadow: 0 4px 24px rgba(0, 212, 255, 0.3);
      transition: all 0.3s ease;
    }

    .btn-cta:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 32px rgba(0, 212, 255, 0.5);
    }

    .social-proof {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-top: 32px;
    }

    .avatars {
      display: flex;
    }

    .avatars img {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      border: 2px solid #0a0e17;
      margin-left: -10px;
    }

    .avatars img:first-child {
      margin-left: 0;
    }

    .social-proof span {
      color: #b8c5d6;
      font-size: 14px;
    }

    /* Seção Pilares */
    .pilares {
      padding: 80px 40px;
    }

    .pilares-title {
      text-align: center;
      font-size: 36px;
      margin-bottom: 48px;
    }

    .pilares-title span {
      color: #00d4ff;
    }

    .pilares-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 24px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .pilar-card {
      position: relative;
      border-radius: 12px;
      overflow: hidden;
      min-height: 320px;
      background: #0d1520;
    }

    .pilar-card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }

    .pilar-card__content {
      padding: 24px;
      display: grid;
      grid-template-columns: 1fr 1.5fr;
      gap: 20px;
    }

    .pilar-label {
      font-family: monospace;
      font-size: 14px;
      color: #5ba3c0;
      margin-bottom: 8px;
    }

    .pilar-title {
      font-size: 24px;
      font-weight: 700;
    }

    .pilar-title span {
      color: #00d4ff;
    }

    .pilar-desc {
      font-size: 14px;
      color: #b8c5d6;
      line-height: 1.6;
      border-left: 1px solid rgba(255,255,255,0.2);
      padding-left: 20px;
    }
  </style>
</head>
<body>
  <section class="hero">
    <div class="hero-content">
      <div class="logo">
        <span class="logo-projeto">PROJETO</span>
        <span class="logo-nome">Nômade Milionário</span>
      </div>

      <h1>
        O método secreto que já movimentou mais de
        <em>1 bilhão em vendas online</em>
      </h1>

      <p class="subtitle">
        Aprenda passo a passo como vender pela internet e criar um negócio lucrativo e automatizado.
      </p>

      <button class="btn-cta">
        QUERO ME INSCREVER
        <span>↗</span>
      </button>

      <div class="social-proof">
        <div class="avatars">
          <img src="avatar1.jpg" alt="">
          <img src="avatar2.jpg" alt="">
          <img src="avatar3.jpg" alt="">
        </div>
        <span>+ de 7000 alunos espalhados pelo mundo</span>
      </div>
    </div>
  </section>

  <section class="pilares">
    <h2 class="pilares-title">Os 4 <span>Pilares</span> do Projeto Nômade Milionário</h2>

    <div class="pilares-grid">
      <div class="pilar-card">
        <img src="pilar1.jpg" alt="Método Passo a Passo">
        <div class="pilar-card__content">
          <div>
            <p class="pilar-label">Pilar 1</p>
            <h3 class="pilar-title">Método Passo a Passo</h3>
          </div>
          <p class="pilar-desc">Aprenda o mesmo processo que já movimentou mais de 1 bilhão em vendas online, do zero até a escala máxima.</p>
        </div>
      </div>

      <div class="pilar-card">
        <img src="pilar2.jpg" alt="Estratégias de Vendas Online">
        <div class="pilar-card__content">
          <div>
            <p class="pilar-label">Pilar 2</p>
            <h3 class="pilar-title"><span>E</span>stratégias de Vendas Online</h3>
          </div>
          <p class="pilar-desc">Modelos prontos de funis e campanhas que você pode aplicar e começar a gerar vendas diárias imediatamente.</p>
        </div>
      </div>

      <div class="pilar-card">
        <img src="pilar3.jpg" alt="Comunidade Exclusiva">
        <div class="pilar-card__content">
          <div>
            <p class="pilar-label">Pilar 3</p>
            <h3 class="pilar-title">Comunidade Exclusiva</h3>
          </div>
          <p class="pilar-desc">Acesso a um grupo fechado de nômades digitais, para networking, insights e suporte contínuo.</p>
        </div>
      </div>

      <div class="pilar-card">
        <img src="pilar4.jpg" alt="Ferramentas e Automação">
        <div class="pilar-card__content">
          <div>
            <p class="pilar-label">Pilar 4</p>
            <h3 class="pilar-title"><span>F</span>erramentas e Automação</h3>
          </div>
          <p class="pilar-desc">Os recursos que tornam seu negócio independente de você, rodando de forma automática, enquanto você ganha tempo e liberdade.</p>
        </div>
      </div>
    </div>
  </section>
</body>
</html>
```

---

## Checklist de Implementação

- [ ] Background escuro (#0a0e17) configurado
- [ ] Gradiente ciano para CTAs
- [ ] Tipografia com pesos variados (400, 600, 700)
- [ ] Headlines com destaque em itálico + ciano
- [ ] Logo composto (sans-serif + script)
- [ ] Botão CTA com sombra glow azul
- [ ] Prova social com avatares
- [ ] Cards de pilares com grid 2x2
- [ ] Labels em estilo monospace
- [ ] Primeira letra destacada em ciano
- [ ] Divisor vertical nos cards
- [ ] Efeito glow de luz ambiente
- [ ] Responsividade mobile
- [ ] Hover states com elevação

---

## Resumo do Estilo

| Aspecto | Característica |
|---------|----------------|
| **Mood** | Premium, Tecnológico, Aspiracional |
| **Tema** | Dark Mode |
| **Cor Principal** | Ciano (#00d4ff) |
| **Tipografia** | Bold headlines, pesos variados |
| **Imagens** | Lifestyle luxo, tom frio |
| **Efeitos** | Glow, Glassmorphism, Gradientes |
| **Conversão** | Números grandes, prova social, CTA destacado |
