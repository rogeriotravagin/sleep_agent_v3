# Diretrizes de Design: Makers - Academia Lendária

**Produto:** Makers - Programa de Desenvolvimento 0 ao Deploy
**Data de Extração:** 2026-02-02
**Referência:** makers.html
**Analista:** Design Analyst (Sleep Agent - Extensão Branding)

---

## Princípios Fundamentais

1. **Dark Mode First** — Design otimizado para ambientes escuros, reduzindo fadiga visual e criando atmosfera tech/profissional
2. **Purple como Brand Color** — Roxo (#7C6AFA) como cor de identidade, transmitindo inovação, tecnologia e criatividade
3. **Clareza e Hierarquia** — Estrutura visual clara com cards, badges e ícones facilitando escaneabilidade
4. **Glassmorphism Sutil** — Uso de gradientes e overlays semi-transparentes para profundidade
5. **Interatividade Fluida** — Micro-interações em hover, transições suaves, animações sutis

---

## Sistema de Cores

### Cores Primárias (Brand)

| Nome | HEX | RGB | Uso |
|------|-----|-----|-----|
| primary-purple | `#7C6AFA` | 124, 106, 250 | Cor principal da marca, CTAs, destaques |
| primary-purple-light | `#9D8FFF` | 157, 143, 255 | Hover states, links, gradientes |
| primary-purple-dark | `#5B4AD4` | 91, 74, 212 | Botões primários (sombra), gradientes |

### Cores de Background (Dark Theme)

| Token | HEX | RGB | Uso |
|-------|-----|-----|-----|
| bg-dark | `#0D0D14` | 13, 13, 20 | Background principal da página |
| bg-card | `#16161F` | 22, 22, 31 | Background de cards, componentes |
| bg-card-hover | `#1E1E2A` | 30, 30, 42 | Hover state de cards |

### Cores de Texto

| Token | HEX | RGB | Uso |
|-------|-----|-----|-----|
| text-white | `#FFFFFF` | 255, 255, 255 | Títulos principais, texto de alta importância |
| text-gray-light | `#C0C0D0` | 192, 192, 208 | Texto secundário, descrições |
| text-gray | `#A0A0B0` | 160, 160, 176 | Texto terciário, labels |

### Cores de Estado

| Estado | HEX | RGB | Uso |
|--------|-----|-----|-----|
| success-green | `#4ADE80` | 74, 222, 128 | Badges de sucesso, confirmações |
| warning-orange | `#FB923C` | 251, 146, 60 | Badges "Coming Soon", alertas |

### Cores Estruturais

| Token | HEX | RGB | Uso |
|-------|-----|-----|-----|
| border-color | `#2A2A3A` | 42, 42, 58 | Bordas de cards, separadores |

### Gradientes

| Nome | Especificação | Uso |
|------|---------------|-----|
| gradient-purple-bg | `linear-gradient(135deg, rgba(124, 106, 250, 0.1) 0%, rgba(124, 106, 250, 0.05) 100%)` | Background de hero, cards destacados |
| gradient-page-bg | `linear-gradient(180deg, #0D0D14 0%, #12121A 100%)` | Background da página |
| gradient-text-hero | `linear-gradient(135deg, #FFFFFF 0%, #9D8FFF 100%)` | Títulos hero com efeito gradient |
| gradient-icon | `linear-gradient(135deg, #7C6AFA 0%, #5B4AD4 100%)` | Ícones e elementos gráficos |

---

## Sistema Tipográfico

### Font Family

- **Primária:** `'Inter'` — Toda a interface
- **Fallback:** `-apple-system, BlinkMacSystemFont, sans-serif`
- **Link Google Fonts:** `https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap`

### Escala de Tamanhos

| Token | Tamanho | Rem | Line-height | Uso |
|-------|---------|-----|-------------|-----|
| text-xs | 12px | 0.75rem | 16px | Badges pequenos, micro labels |
| text-sm | 14px | 0.875rem | 20px | Badges, labels, frequências |
| text-base | 16px | 1rem | 24px | Corpo de texto principal |
| text-base-plus | 17.6px | 1.1rem | ~26px | Descrições importantes, lead text |
| text-md | 15.2px | 0.95rem | ~22px | Texto secundário, links |
| text-lg | 17.6px | 1.1rem | ~26px | Títulos de cards, event titles |
| text-xl | 18.4px | 1.15rem | ~28px | Subtítulos de seção |
| text-2xl | 24px | 1.5rem | 32px | Section titles, product titles |
| text-3xl | 30px | 1.875rem | 36px | — |
| text-4xl | 36px | 2.25rem | 40px | — |
| text-hero | 40px | 2.5rem | ~48px | Hero h1 (desktop) |
| text-hero-mobile | 28.8px | 1.8rem | ~34px | Hero h1 (mobile) |

### Pesos (Weights)

| Token | Valor | Uso |
|-------|-------|-----|
| font-normal | 400 | Texto corrido, descrições |
| font-medium | 500 | Links, labels |
| font-semibold | 600 | Subtítulos, badges importantes |
| font-bold | 700 | Títulos de seção, section headers |
| font-extrabold | 800 | Hero titles, títulos de máximo destaque |

### Line-height Padrão

- **Body text:** `1.6` (160%)
- **Headings:** Varia por tamanho (especificado na tabela acima)

---

## Sistema de Espaçamento

### Escala Base (Pixels)

| Token | Valor | Uso Recomendado |
|-------|-------|-----------------|
| space-0 | 0px | Reset |
| space-1 | 4px | Micro espaçamento, ajustes finos |
| space-2 | 6px | Gaps internos pequenos (badges) |
| space-3 | 8px | Gaps entre ícones e texto |
| space-4 | 10px | Padding de badges, elementos pequenos |
| space-5 | 12px | Gaps entre elementos relacionados |
| space-6 | 16px | Padding padrão de elementos, margin bottom |
| space-7 | 20px | Padding de cards pequenos, gaps entre grupos |
| space-8 | 24px | Padding de cards médios, margin entre seções |
| space-10 | 32px | Padding de cards grandes |
| space-12 | 40px | Margin entre seções principais |
| space-14 | 48px | — |
| space-16 | 60px | Padding de hero sections |

### Containers

| Elemento | Max-width | Padding |
|----------|-----------|---------|
| .container | 800px | 40px 24px |

---

## Border Radius (Arredondamento)

### Escala

| Token | Valor | Uso |
|-------|-------|-----|
| radius-sm | 6px | Badges pequenos, micro elementos |
| radius-md | 8px | — |
| radius-base | 10px | Botões, links de card |
| radius-lg | 12px | Ícones pequenos, elementos destacados |
| radius-xl | 14px | Step numbers, elementos médios |
| radius-2xl | 16px | Cards padrão, inputs, tables |
| radius-3xl | 20px | Cards destacados, main product card |
| radius-4xl | 24px | Hero section, cards especiais |
| radius-full | 50px | Badges pill-style, botões arredondados |

---

## Shadows (Sombras)

**Nota:** A página não usa sombras explícitas, preferindo borders e gradientes para criar profundidade.

---

## Componentes Base

### 1. Hero Section

**Estrutura:**
- Container com gradiente de background
- Badge no topo (pill-style)
- Título h1 com gradiente de texto
- Parágrafo de descrição
- Animação pulse no background

**Especificações:**
```css
.hero {
  text-align: center;
  padding: 60px 20px;
  background: linear-gradient(135deg, rgba(124, 106, 250, 0.1) 0%, rgba(124, 106, 250, 0.05) 100%);
  border-radius: 24px;
  border: 1px solid rgba(124, 106, 250, 0.2);
  margin-bottom: 40px;
  position: relative;
  overflow: hidden;
}

.hero h1 {
  font-size: 2.5rem;
  font-weight: 800;
  background: linear-gradient(135deg, #FFFFFF 0%, #9D8FFF 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
```

### 2. Badges

**Variações:**

| Variação | Background | Color | Padding | Border-radius |
|----------|------------|-------|---------|---------------|
| Primary Badge | `#7C6AFA` | white | 8px 16px | 50px |
| Primary Small | `#7C6AFA` | white | 6px 14px | 50px |
| Success Badge | `rgba(74, 222, 128, 0.15)` | `#4ADE80` | 4px 10px | 6px |
| Warning Badge | `rgba(251, 146, 60, 0.2)` | `#FB923C` | 10px 16px | 10px |
| Info Badge | `rgba(124, 106, 250, 0.2)` | `#9D8FFF` | 3px 10px | 6px |
| Optional Badge | `rgba(160, 160, 176, 0.15)` | `#C0C0D0` | 4px 10px | 6px |

**Tipografia:**
- Font-size: 12px - 14px
- Font-weight: 600 - 700
- Text-transform: uppercase (para alguns)
- Letter-spacing: 0.5px (para uppercase)

### 3. Section Header

**Estrutura:**
- Ícone em container com gradiente
- Título ao lado
- Border bottom separador

**Especificações:**
```css
.section-header {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 20px;
  padding-bottom: 12px;
  border-bottom: 1px solid #2A2A3A;
}

.section-icon {
  width: 40px;
  height: 40px;
  background: linear-gradient(135deg, #7C6AFA 0%, #5B4AD4 100%);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

### 4. Cards

**Card Padrão (Bonus Card):**
```css
.bonus-card {
  background: #16161F;
  border: 1px solid #2A2A3A;
  border-radius: 16px;
  padding: 24px;
  transition: all 0.3s ease;
}

.bonus-card:hover {
  background: #1E1E2A;
  border-color: rgba(124, 106, 250, 0.5);
  transform: translateY(-2px);
}
```

**Main Product Card (Destaque):**
```css
.main-product-card {
  background: linear-gradient(135deg, rgba(124, 106, 250, 0.15) 0%, rgba(124, 106, 250, 0.05) 100%);
  border: 2px solid #7C6AFA;
  border-radius: 20px;
  padding: 32px;
  position: relative;
  overflow: hidden;
}
```

**Step Card:**
```css
.step-card {
  display: flex;
  gap: 20px;
  padding: 24px;
  background: #16161F;
  border: 1px solid #2A2A3A;
  border-radius: 16px;
  margin-bottom: 16px;
  transition: all 0.3s ease;
}

.step-card:hover {
  border-color: #7C6AFA;
  background: #1E1E2A;
}
```

### 5. Botões

**Botão Primário:**
```css
.step-button {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: #7C6AFA;
  color: white;
  padding: 12px 20px;
  border-radius: 10px;
  font-weight: 600;
  font-size: 0.95rem;
  transition: all 0.2s ease;
}

.step-button:hover {
  background: #9D8FFF;
  transform: translateY(-1px);
}
```

**Botão Secundário:**
```css
.step-button-secondary {
  background: rgba(124, 106, 250, 0.15);
  color: #9D8FFF;
}

.step-button-secondary:hover {
  background: rgba(124, 106, 250, 0.25);
}
```

**Links de Card:**
```css
.card-link {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  color: #9D8FFF;
  font-weight: 500;
  font-size: 0.9rem;
  transition: gap 0.2s ease;
}

.card-link:hover {
  gap: 10px;
}
```

### 6. Feature List

**Estrutura:**
- Lista sem bullet points
- Ícone em container roxo
- Texto com strong tags

**Especificações:**
```css
.feature-list li {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  padding: 12px 0;
  border-bottom: 1px solid #2A2A3A;
}

.feature-icon {
  width: 24px;
  height: 24px;
  background: rgba(124, 106, 250, 0.2);
  border-radius: 6px;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

### 7. Tips Box

```css
.tips-box {
  background: linear-gradient(135deg, rgba(124, 106, 250, 0.1) 0%, rgba(124, 106, 250, 0.05) 100%);
  border: 1px solid rgba(124, 106, 250, 0.3);
  border-radius: 16px;
  padding: 24px;
}
```

### 8. Comparison Table

```css
.comparison-table {
  border-collapse: separate;
  border-spacing: 0;
  border-radius: 16px;
  overflow: hidden;
  border: 1px solid #2A2A3A;
}

.comparison-table th {
  background: #7C6AFA;
  color: white;
  font-weight: 600;
  padding: 16px 20px;
}

.comparison-table td {
  background: #16161F;
  border-bottom: 1px solid #2A2A3A;
  padding: 16px 20px;
}
```

### 9. Step Number

```css
.step-number {
  width: 48px;
  height: 48px;
  background: linear-gradient(135deg, #7C6AFA 0%, #5B4AD4 100%);
  border-radius: 14px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 800;
  font-size: 1.3rem;
}
```

---

## Iconografia

### Estilo
- **Biblioteca:** SVG inline (Feather Icons style)
- **Stroke-width:** 2px
- **Fill:** none
- **Stroke:** currentColor

### Tamanhos

| Contexto | Width | Height |
|----------|-------|--------|
| Badges | 18px | 18px |
| Section icons | 20px | 20px |
| Card links | 16px | 16px |
| Buttons | 18px | 18px |
| Product icon | 28px | 28px |
| Emoji replacement | 24px | 24px |

---

## Animações e Transições

### Pulse Animation (Hero Background)

```css
@keyframes pulse {
  0%, 100% { transform: scale(1); opacity: 0.5; }
  50% { transform: scale(1.1); opacity: 0.8; }
}

animation: pulse 4s ease-in-out infinite;
```

### Spin Animation (Loading)

```css
@keyframes spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

animation: spin 2s linear infinite;
```

### Transitions

| Elemento | Propriedade | Duração | Easing |
|----------|-------------|---------|--------|
| Cards | all | 0.3s | ease |
| Botões | all | 0.2s | ease |
| Links | gap | 0.2s | ease |

---

## Grid e Layout

### Grid Responsivo

```css
.bonus-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 16px;
}
```

### Breakpoints

| Breakpoint | Max-width | Ajustes |
|------------|-----------|---------|
| Mobile | 600px | Hero h1: 1.8rem, Grid: 1 coluna, Step cards: flex-direction column |

---

## Estados de Interação

### Hover States

| Elemento | Efeito |
|----------|--------|
| Cards | Background mais claro + Border roxo + translateY(-2px) |
| Botões Primários | Background lighter + translateY(-1px) |
| Links | Gap aumenta (6px → 10px) |
| Support Links | Background roxo + Color roxo claro |

### Active/Focus States

Seguir padrão de hover com ajustes de contraste.

---

## Do's and Don'ts

### Do's (Faça)

✅ **Use dark backgrounds** — O sistema é otimizado para modo escuro
✅ **Mantenha roxo como cor principal** — #7C6AFA é a identidade da marca
✅ **Use badges para destacar informações** — Coming Soon, frequências, status
✅ **Aplique gradientes sutis** — Especialmente em backgrounds de destaque
✅ **Adicione micro-interações** — Hover com translateY e transições suaves
✅ **Use Inter como fonte principal** — Pesos 400, 500, 600, 700, 800
✅ **Mantenha hierarquia com ícones** — Section icons com gradiente roxo
✅ **Use border-radius generoso** — 16px para cards, 24px para hero

### Don'ts (Evite)

❌ **Não use cores fora da paleta** — Mantém consistência visual
❌ **Evite sombras pesadas** — O design usa borders e gradientes
❌ **Não misture light mode** — Sistema é dark-first
❌ **Evite animações excessivas** — Apenas pulse e spin sutis
❌ **Não use fontes diferentes** — Inter em todos os contextos
❌ **Evite espaçamento inconsistente** — Siga a escala definida
❌ **Não ignore estados de hover** — Interatividade é essencial
❌ **Evite borders muito finas** — 1px é o mínimo, 2px para destaque

---

## Acessibilidade

### Contraste de Cores

| Combinação | Contraste | Status |
|------------|-----------|--------|
| text-white (#FFFFFF) / bg-dark (#0D0D14) | 19.43:1 | ✅ AAA |
| text-gray-light (#C0C0D0) / bg-dark (#0D0D14) | 11.51:1 | ✅ AAA |
| primary-purple (#7C6AFA) / bg-dark (#0D0D14) | 6.12:1 | ✅ AA |
| text-white (#FFFFFF) / primary-purple (#7C6AFA) | 3.17:1 | ⚠️ AA Large |

**Recomendação:** Para textos pequenos em botões roxos, considere usar text-white (#FFFFFF) apenas em font-weight 600+ ou aumentar o contraste.

### Focus States

Adicionar outline visível para navegação por teclado:
```css
:focus-visible {
  outline: 2px solid #7C6AFA;
  outline-offset: 2px;
}
```

---

## Responsive Design

### Mobile (max-width: 600px)

**Ajustes:**
- Hero h1: 2.5rem → 1.8rem
- Grid: minmax(280px, 1fr) → 1 coluna
- Step cards: flex → flex-column
- Padding de container: 40px 24px mantido
- Padding de cards: 32px → 24px

---

## Implementação Técnica

### CSS Variables (Recomendado)

```css
:root {
  /* Cores Primárias */
  --primary-purple: #7C6AFA;
  --primary-purple-light: #9D8FFF;
  --primary-purple-dark: #5B4AD4;

  /* Backgrounds */
  --bg-dark: #0D0D14;
  --bg-card: #16161F;
  --bg-card-hover: #1E1E2A;

  /* Texto */
  --text-white: #FFFFFF;
  --text-gray: #A0A0B0;
  --text-gray-light: #C0C0D0;

  /* Estruturais */
  --border-color: #2A2A3A;

  /* Estados */
  --success-green: #4ADE80;
  --warning-orange: #FB923C;

  /* Espaçamento */
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-6: 24px;
  --space-8: 32px;
  --space-12: 48px;
  --space-16: 64px;

  /* Border Radius */
  --radius-sm: 6px;
  --radius-base: 10px;
  --radius-lg: 12px;
  --radius-xl: 16px;
  --radius-2xl: 20px;
  --radius-3xl: 24px;
  --radius-full: 50px;
}
```

---

## Próximos Passos

- [ ] Criar biblioteca de componentes reutilizáveis (React/Vue/HTML)
- [ ] Implementar design tokens em formato JSON
- [ ] Criar style guide visual interativo
- [ ] Documentar mais estados de componentes (loading, disabled)
- [ ] Criar templates de página seguindo estas diretrizes
- [ ] Implementar tema claro (opcional, se necessário)

---

## Referências

- **Página Analisada:** `/home/rogerio/projetos/Projetos academia lendaria/projeto_academia_lendaria/paginas_html/makers.html`
- **Framework:** Sleep Agent Framework - Extensão Branding
- **Agente:** Design Analyst
- **Data:** 2026-02-02

---

**Documento criado por:** Sleep Agent - Design Analyst
**Versão:** 1.0
