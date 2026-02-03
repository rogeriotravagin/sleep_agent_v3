# Diretrizes de Design: Cohort Fundamentals

**Produto:** Sistema de Grade Curricular Pedagógica - Academia Lendária
**URL Referência:** https://cohorts.academialendaria.ai/
**Data da Análise:** 2026-02-02
**Versão:** 2.0 (Atualizado baseado na logo oficial)

---

## Princípios Fundamentais

1. **Profundidade e Fundação através de Gradientes Orgânicos**
   - Design dark-mode baseado em gradientes teal-to-black que evocam profundidade
   - Uso de teal/verde-azulado como cor primária representando fundamentos sólidos e crescimento

2. **Minimalismo Moderno com Identidade Forte**
   - Tipografia em cápsulas pill-shaped (bordas arredondadas completas)
   - Interface limpa e focada com elementos pill que criam hierarquia visual
   - Bordas brancas sutis que definem espaços sem peso visual excessivo

3. **Estrutura Modular Expansível**
   - Gradientes de fundo que criam profundidade sem ruído visual
   - Estrutura modular e expansível (collapsible sections)
   - Transições suaves que mantêm a fluidez orgânica do design

---

## Sistema de Cores

### Cores Primárias

| Nome | HEX | RGB | Uso |
|------|-----|-----|-----|
| primary-teal | `#14B8A6` | 20, 184, 166 | Ações principais, brand identity, destaques fundamentais |
| secondary-teal-dark | `#0D9488` | 13, 148, 136 | Hover states, elementos secundários, profundidade |
| accent-teal-deep | `#134E4A` | 19, 78, 74 | Gradientes de fundo, módulos de profundidade |
| accent-white | `#FFFFFF` | 255, 255, 255 | Bordas, texto principal, pills/cápsulas |

### Cores de Background (Dark Mode)

| Token | HEX | Uso |
|-------|-----|-----|
| bg-primary | `#000000` | Background principal (preto puro) |
| bg-gradient-start | `#000000` | Início do gradiente (preto) |
| bg-gradient-end | `#0A2E2C` | Fim do gradiente (teal muito escuro) |
| bg-secondary | `#0F0F0F` | Superfícies elevadas (sidebar) |
| bg-card | `#1A1A1A` | Background de cards |
| bg-card-hover | `rgba(20, 184, 166, 0.05)` | Background de cards em hover (teal sutil) |
| bg-modal | `#252525` | Modais e dropdowns |

### Cores de Estado

| Estado | HEX | Uso |
|--------|-----|-----|
| success | `#22C55E` | Confirmações, progresso completo |
| warning | `#EAB308` | Alertas, atenção |
| error | `#EF4444` | Erros, bloqueios |
| info | `#3B82F6` | Informações neutras |

### Cores Neutras (Texto)

| Token | HEX | Uso |
|-------|-----|-----|
| text-primary | `#FFFFFF` | Títulos, texto principal |
| text-secondary | `#A3A3A3` | Texto de suporte |
| text-muted | `#6B7280` | Captions, metadados |

### Borders

| Token | HEX | Uso |
|-------|-----|-----|
| border-standard | `#2A2A2A` | Borders padrão |
| border-light | `#3A3A3A` | Borders mais claros |
| border-teal | `#14B8A6` | Borders de destaque (pills, foco) |
| border-white | `#FFFFFF` | Borders de cápsulas/pills principais |

### Gradientes Característicos

| Nome | Código CSS | Uso |
|------|------------|-----|
| Hero Gradient | `linear-gradient(180deg, #000000 0%, #0A2E2C 100%)` | Background principal, hero sections |
| Card Gradient Hover | `linear-gradient(135deg, rgba(20, 184, 166, 0.08) 0%, transparent 100%)` | Hover state de cards |
| Radial Teal Glow | `radial-gradient(circle at center, rgba(20, 184, 166, 0.15), transparent 70%)` | Efeitos de profundidade |
| Pill Background | `radial-gradient(ellipse at center, rgba(20, 184, 166, 0.1), transparent)` | Background interno de pills importantes |

---

## Sistema Tipográfico

### Font Family

- **Primária:** `'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`
- **Uso:** Toda interface - tipografia moderna e legível

### Escala de Tamanhos

| Token | Tamanho | Line-height | Uso |
|-------|---------|-------------|-----|
| text-xs | 12px (0.75rem) | 16px | Captions, labels pequenos |
| text-sm | 14px (0.875rem) | 20px | Labels, texto auxiliar |
| text-base | 16px (1rem) | 24px | Corpo de texto |
| text-lg | 18px (1.125rem) | 28px | Lead paragraphs |
| text-xl | 20px (1.25rem) | 28px | H4, subtítulos |
| text-2xl | 24px (1.5rem) | 32px | H3 |
| text-3xl | 30px (1.875rem) | 36px | H2, métricas destacadas |
| text-4xl | 36px (2.25rem) | 40px | H1 |
| text-5xl | 48px (3rem) | 1 | Display, hero titles |

### Pesos

| Token | Valor | Uso |
|-------|-------|-----|
| font-normal | 400 | Texto corrido |
| font-medium | 500 | Ênfase leve, labels |
| font-semibold | 600 | Subtítulos |
| font-bold | 700 | Títulos, destaques fortes |

---

## Sistema de Espaçamento

### Escala Base (Sistema de 8pt)

| Token | Valor | Uso Recomendado |
|-------|-------|-----------------|
| space-0 | 0 | Reset |
| space-1 | 4px (0.25rem) | Micro espaçamento |
| space-2 | 8px (0.5rem) | Interno de componentes pequenos |
| space-3 | 12px (0.75rem) | Entre elementos relacionados |
| space-4 | 16px (1rem) | Padding padrão |
| space-6 | 24px (1.5rem) | Entre grupos de elementos |
| space-8 | 32px (2rem) | Entre seções pequenas |
| space-10 | 40px (2.5rem) | Entre seções médias |
| space-12 | 48px (3rem) | Entre blocos grandes |
| space-16 | 64px (4rem) | Entre seções principais |

---

## Layout & Grid

### Sidebar Navigation

| Propriedade | Valor |
|-------------|-------|
| Width | 220px |
| Position | Fixed left |
| Background | `#0F0F0F` |
| Breakpoint Mobile | < 768px (ocultar) |

**Estados de Link:**
- Default: texto `#A3A3A3`
- Hover: borda esquerda sutil
- Active: borda esquerda gold `#C9A227`

### Main Content

| Propriedade | Valor |
|-------------|-------|
| Margin-left | 220px (offset da sidebar) |
| Max-width | 1200px |
| Padding | `1.5rem` a `2rem` |

### Grid Systems

**Auto-fit Grid (Responsivo)**
```css
display: grid;
grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
gap: 1.5rem;
```

**Variações:**
- 2 colunas: `minmax(300px, 1fr)`
- 3 colunas: `minmax(200px, 1fr)`
- 4 colunas: `minmax(140px, 1fr)`

---

## Componentes Base

### Pills/Cápsulas (Novo Componente Característico)

| Propriedade | Valor |
|-------------|-------|
| Background | Transparente ou `rgba(20, 184, 166, 0.1)` |
| Border-radius | `9999px` (pill completo) |
| Padding | `0.75rem 1.5rem` ou `1rem 2rem` (conforme tamanho) |
| Border | `2px solid #FFFFFF` ou `2px solid #14B8A6` |
| Font-weight | 500 (medium) a 600 (semibold) |

**Variantes:**
- **Hero Pill:** Border branca (`#FFFFFF`), texto branco, background com gradiente teal sutil
- **Interactive Pill:** Border teal (`#14B8A6`), hover com glow teal
- **Label Pill:** Menor, border mais fina (1px), text-sm

**Estados:**
- Default: Border sólida, sem background ou background muito sutil
- Hover: Glow teal externo, background intensifica levemente
- Active: Background teal (`#14B8A6`), texto preto (`#000000`)

### Cards/Módulos

| Propriedade | Valor |
|-------------|-------|
| Background | `#1A1A1A` ou gradiente sutil |
| Border-radius | `1rem` (16px) a `1.5rem` (24px) |
| Padding | `1.5rem` a `2rem` |
| Border | `1px solid #2A2A2A` |

**Estados:**
- Default: border padrão
- Hover: border-color shift para teal (`#14B8A6`), elevação `-2px` Y-axis, background com gradiente teal
- Collapsible: ícone de seta, transição `0.2s ease`

**Variações de Borda Lateral (Accent):**
- Teal (`#14B8A6`): Conteúdo prioritário, fundamentos
- Teal Dark (`#0D9488`): Conteúdo secundário
- Teal Deep (`#134E4A`): Módulos de profundidade nível 1

### Botões

| Propriedade | Valor |
|-------------|-------|
| Border-radius | `9999px` (pill shape) ou `0.75rem` (12px) |
| Padding | `0.75rem 1.5rem` |
| Font-weight | 500 (medium) |
| Transition | `0.2s ease` |

**Variantes:**

**Primary (Teal):**
- Background: `#14B8A6`
- Text: `#000000`
- Hover: background `#0D9488`, glow teal sutil
- Border-radius: `9999px` (pill preferencial)

**Primary Outline:**
- Background: transparente
- Border: `2px solid #14B8A6`
- Text: `#14B8A6`
- Hover: background `rgba(20, 184, 166, 0.1)`
- Border-radius: `9999px`

**Secondary:**
- Background: `#252525`
- Text: `#FFFFFF`
- Hover: background `#2A2A2A`, border `1px solid #3A3A3A`

**Ghost:**
- Background: transparente
- Border: `1px solid #3A3A3A`
- Text: `#FFFFFF`
- Hover: background `#1A1A1A`, border-color `#14B8A6`

### Badges

| Propriedade | Valor |
|-------------|-------|
| Border-radius | `9999px` (pill shape) |
| Padding | `0.25rem 0.75rem` |
| Font-size | `0.75rem` |
| Font-weight | 500 |
| Border | Opcional: `1px solid [cor correspondente]` |

**Variantes:**
- **Primary Teal:** bg `rgba(20, 184, 166, 0.15)`, text `#14B8A6`, border opcional `#14B8A6`
- **Teal Dark:** bg `rgba(13, 148, 136, 0.15)`, text `#0D9488`
- **Success:** bg `rgba(34, 197, 94, 0.15)`, text `#22C55E`
- **Warning:** bg `rgba(234, 179, 8, 0.15)`, text `#EAB308`
- **Danger:** bg `rgba(239, 68, 68, 0.15)`, text `#EF4444`
- **Info:** bg `rgba(59, 130, 246, 0.15)`, text `#3B82F6`

### Inputs/Forms

| Propriedade | Valor |
|-------------|-------|
| Background | `#1A1A1A` |
| Border | `1px solid #2A2A2A` |
| Border-radius | `0.75rem` ou `9999px` (pill para buscas) |
| Padding | `0.75rem 1rem` |
| Font-size | `1rem` |

**Estados:**
- Default: border `#2A2A2A`
- Focus: border `#14B8A6` (`2px`), outline teal glow `0 0 0 3px rgba(20, 184, 166, 0.1)`
- Error: border `#EF4444`
- Success: border `#22C55E`
- Disabled: opacity `0.5`, cursor not-allowed

### Métricas Dashboard

| Propriedade | Valor |
|-------------|-------|
| Background | `#1A1A1A` |
| Border-radius | `1rem` |
| Padding | `1.5rem` |
| Grid | auto-fit, minmax(140px, 1fr) |

**Variante Highlight:**
- Background: linear-gradient teal (`linear-gradient(135deg, rgba(20, 184, 166, 0.1), transparent)`)
- Border-left: `3px solid #14B8A6` (opcional)
- Valor: `text-3xl`, bold, color `#14B8A6`
- Label: `text-sm`, muted

### Progress Steps

| Propriedade | Valor |
|-------------|-------|
| Circle size | 44px |
| Border | `2px solid #3A3A3A` |
| Font-size | `1rem` |

**Estados:**
- Inactive: border `#3A3A3A`, text `#6B7280`
- Active: background `#14B8A6`, text `#000000`, box-shadow teal glow `0 0 15px rgba(20, 184, 166, 0.3)`
- Completed: background `#22C55E` ou teal com checkmark

**Connector Line:**
- Height: `2px`
- Color: `#3A3A3A`
- Active/Completed: `#14B8A6`

---

## Efeitos Visuais

### Sombras (Dark Mode)

| Uso | Shadow |
|-----|--------|
| Subtle | `0 1px 2px rgba(0,0,0,0.3)` |
| Card | `0 4px 6px rgba(0,0,0,0.4)` |
| Elevated | `0 10px 25px rgba(0,0,0,0.5)` |

### Glows (Accent)

| Cor | Shadow |
|-----|--------|
| Teal Primary | `0 0 20px rgba(20, 184, 166, 0.2)` |
| Teal Subtle | `0 0 15px rgba(20, 184, 166, 0.1)` |
| Teal Strong | `0 0 30px rgba(20, 184, 166, 0.3)` |

### Gradientes (Atualizados)

**Hero/Background Principal:**
```css
background: linear-gradient(180deg, #000000 0%, #0A2E2C 100%);
```

**Radial Teal Glow (Center Focus):**
```css
background: radial-gradient(circle at center, rgba(20, 184, 166, 0.15), transparent 70%);
```

**Card Hover:**
```css
background: linear-gradient(135deg, rgba(20, 184, 166, 0.08) 0%, transparent 100%);
```

**Pill Background:**
```css
background: radial-gradient(ellipse at center, rgba(20, 184, 166, 0.1), transparent);
```

### Transições

| Elemento | Transition |
|----------|-----------|
| Padrão | `0.2s ease` |
| Hover elevado | `0.3s ease` |
| Transform Y | `-2px` (elevação) |

---

## Do's and Don'ts

### Do's (Faça)

- ✅ Use o sistema de 8pt para todos os espaçamentos
- ✅ Mantenha contraste mínimo de 4.5:1 para texto em dark mode
- ✅ Use teal (`#14B8A6`) como cor primária para brand e ações principais
- ✅ Use componentes pill/cápsula (border-radius: 9999px) para elementos importantes
- ✅ Aplique gradientes teal-to-black em backgrounds hero e principais
- ✅ Mantenha hierarquia visual através de tamanho, peso e cor
- ✅ Use transições sutis (0.2s-0.3s) para interações
- ✅ Use borders brancas (`#FFFFFF`) para pills de destaque
- ✅ Use badges com backgrounds semi-transparentes
- ✅ Mantenha cards com hover states que incluam glow teal
- ✅ Use glows teal para criar profundidade e foco

### Don'ts (Evite)

- ❌ Não use cores saturadas demais que competem com o teal
- ❌ Não misture valores de espaçamento fora do sistema de 8pt
- ❌ Não use múltiplas cores primárias competindo por atenção
- ❌ Não crie pills sem border ou com cantos quadrados
- ❌ Não crie cards sem hover states
- ❌ Não use transições longas (> 0.3s)
- ❌ Não ignore os gradientes característicos do brand
- ❌ Não use texto `#FFFFFF` sobre backgrounds claros
- ❌ Não crie componentes sem estados (hover, active, disabled)
- ❌ Não use gold ou cores que conflitem com a identidade teal

---

## Acessibilidade

### Contraste de Cores

| Combinação | Ratio | Status |
|------------|-------|--------|
| `#FFFFFF` sobre `#000000` | 21.0:1 | ✅ AAA |
| `#14B8A6` sobre `#000000` | 5.8:1 | ✅ AA |
| `#A3A3A3` sobre `#000000` | 6.5:1 | ✅ AA |
| `#6B7280` sobre `#000000` | 4.6:1 | ✅ AA |
| `#000000` sobre `#14B8A6` | 3.6:1 | ⚠️ AA Large Text Only |

### Recomendações

- Use texto `#FFFFFF` para títulos e conteúdo principal
- Use `#A3A3A3` para texto secundário
- Use `#6B7280` apenas para metadados/captions
- Garanta focus states visíveis com outline teal glow (`0 0 0 3px rgba(20, 184, 166, 0.1)`)
- Mantenha área de clique mínima de 44x44px
- Use texto preto (`#000000`) sobre backgrounds teal (`#14B8A6`) para garantir contraste
- Em botões teal, sempre use texto preto para máximo contraste

---

## Design Tokens (CSS Variables)

```css
:root {
  /* Colors - Primary (Teal Brand) */
  --color-primary-teal: #14B8A6;
  --color-secondary-teal-dark: #0D9488;
  --color-accent-teal-deep: #134E4A;
  --color-accent-white: #FFFFFF;

  /* Colors - Background */
  --color-bg-primary: #000000;
  --color-bg-gradient-start: #000000;
  --color-bg-gradient-end: #0A2E2C;
  --color-bg-secondary: #0F0F0F;
  --color-bg-card: #1A1A1A;
  --color-bg-card-hover: rgba(20, 184, 166, 0.05);
  --color-bg-modal: #252525;

  /* Colors - State */
  --color-success: #22C55E;
  --color-warning: #EAB308;
  --color-error: #EF4444;
  --color-info: #3B82F6;

  /* Colors - Text */
  --color-text-primary: #FFFFFF;
  --color-text-secondary: #A3A3A3;
  --color-text-muted: #6B7280;

  /* Colors - Border */
  --color-border-standard: #2A2A2A;
  --color-border-light: #3A3A3A;
  --color-border-teal: #14B8A6;
  --color-border-white: #FFFFFF;

  /* Spacing */
  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-6: 1.5rem;
  --space-8: 2rem;
  --space-10: 2.5rem;
  --space-12: 3rem;
  --space-16: 4rem;

  /* Typography */
  --font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --font-weight-normal: 400;
  --font-weight-medium: 500;
  --font-weight-semibold: 600;
  --font-weight-bold: 700;

  /* Border Radius */
  --radius-sm: 0.5rem;
  --radius-md: 0.75rem;
  --radius-lg: 1rem;
  --radius-xl: 1.5rem;
  --radius-full: 9999px;

  /* Shadows */
  --shadow-subtle: 0 1px 2px rgba(0,0,0,0.3);
  --shadow-card: 0 4px 6px rgba(0,0,0,0.4);
  --shadow-elevated: 0 10px 25px rgba(0,0,0,0.5);
  --shadow-glow-teal: 0 0 20px rgba(20, 184, 166, 0.2);
  --shadow-glow-teal-subtle: 0 0 15px rgba(20, 184, 166, 0.1);
  --shadow-glow-teal-strong: 0 0 30px rgba(20, 184, 166, 0.3);

  /* Gradients */
  --gradient-hero: linear-gradient(180deg, #000000 0%, #0A2E2C 100%);
  --gradient-card-hover: linear-gradient(135deg, rgba(20, 184, 166, 0.08) 0%, transparent 100%);
  --gradient-radial-teal: radial-gradient(circle at center, rgba(20, 184, 166, 0.15), transparent 70%);
  --gradient-pill-bg: radial-gradient(ellipse at center, rgba(20, 184, 166, 0.1), transparent);

  /* Transitions */
  --transition-fast: 0.2s ease;
  --transition-normal: 0.3s ease;
}
```

---

## Estrutura Atômica (Atomic Design)

### Átomos
- Color tokens
- Tipografia base
- Botões primitivos
- Badges
- Ícones

### Moléculas
- Cards de métrica
- Progress steps
- Callouts
- Checklists
- Cards de aula

### Organismos
- Header com progresso
- Sidebar de navegação
- Módulos expandíveis
- Visualização iceberg
- Dashboard de métricas

### Templates
- Layout principal (sidebar + content)
- Grid systems responsivos
- Boxes de transformação
- Estruturas de página

---

## Próximos Passos

- [ ] Criar biblioteca de componentes React/Vue baseada nestas diretrizes
- [ ] Implementar design tokens em código (CSS/JS)
- [ ] Criar style guide visual interativo
- [ ] Documentar padrões de animação e micro-interações
- [ ] Estabelecer guidelines de responsividade detalhados
- [ ] Criar protótipos de novos componentes seguindo o sistema

---

## Referências

**Metodologias Aplicadas:**
- **Grid Systems** (Josef Muller-Brockmann): Estrutura modular consistente
- **10 Principles of Good Design** (Dieter Rams): Minimalismo funcional
- **Atomic Design** (Brad Frost): Hierarquia de componentes
- **Material Design** (Google): Sistema de 8pt spacing
- **Dark Mode Best Practices**: Contraste e hierarquia visual

**URL Analisada:** https://cohorts.academialendaria.ai/

---

**Autor:** Design Analyst - Sleep Agent
**Extensão:** Branding & Visual v1.0
**Última Atualização:** 2026-02-02
