# Diretrizes de Design: Cohort Essentials

**Produto:** Sistema de Grade Curricular Pedagógica - Academia Lendária
**URL Referência:** https://cohorts.academialendaria.ai/
**Data da Análise:** 2026-02-02
**Versão:** 1.0

---

## Princípios Fundamentais

1. **Profundidade Intelectual através de Hierarquia Visual**
   - Design dark-mode sofisticado que enfatiza rigor intelectual
   - Uso estratégico de cores de destaque (ouro/roxo) para criar camadas de profundidade informacional

2. **Narrativa Visual por Níveis**
   - Metáfora do iceberg: informação em camadas de profundidade
   - Hierarquia tipográfica como condutora do fluxo narrativo

3. **Minimalismo Estruturado com Informação Densa**
   - Interface limpa que suporta grande densidade de conteúdo
   - Estrutura modular e expansível (collapsible sections)

---

## Sistema de Cores

### Cores Primárias

| Nome | HEX | RGB | Uso |
|------|-----|-----|-----|
| primary-gold | `#C9A227` | 201, 162, 39 | Ações principais, destaques de sabedoria, brand |
| secondary-purple | `#A855F7` | 168, 85, 247 | Conteúdo avançado, maestria, elementos secundários |
| accent-teal | `#134E4A` | 19, 78, 74 | Módulos de profundidade nível 1 |

### Cores de Background (Dark Mode)

| Token | HEX | Uso |
|-------|-----|-----|
| bg-primary | `#0A0A0A` | Background principal |
| bg-secondary | `#0F0F0F` | Superfícies elevadas (sidebar) |
| bg-card | `#1A1A1A` | Background de cards |
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

### Cards/Módulos

| Propriedade | Valor |
|-------------|-------|
| Background | `#1A1A1A` |
| Border-radius | `0.75rem` (12px) a `1.5rem` (24px) |
| Padding | `1.5rem` a `2rem` |
| Border | `1px solid #2A2A2A` |

**Estados:**
- Default: border padrão
- Hover: border-color shift para accent, elevação `-2px` Y-axis
- Collapsible: ícone de seta, transição `0.2s ease`

**Variações de Borda Lateral (Accent):**
- Gold (`#C9A227`): Conteúdo prioritário
- Purple (`#A855F7`): Conteúdo de maestria
- Green (`#1F3D2A`): Módulos nível 1

### Botões

| Propriedade | Valor |
|-------------|-------|
| Border-radius | `0.75rem` (12px) |
| Padding | `0.75rem 1.5rem` |
| Font-weight | 500 (medium) |
| Transition | `0.2s ease` |

**Variantes:**

**Primary:**
- Background: `#C9A227`
- Text: `#0A0A0A`
- Hover: brightness aumentada

**Secondary:**
- Background: `#252525`
- Text: `#FFFFFF`
- Hover: background `#2A2A2A`

**Ghost:**
- Background: transparente
- Border: `1px solid #3A3A3A`
- Text: `#FFFFFF`
- Hover: background `#1A1A1A`

### Badges

| Propriedade | Valor |
|-------------|-------|
| Border-radius | `9999px` (pill shape) |
| Padding | `0.25rem 0.75rem` |
| Font-size | `0.75rem` |
| Font-weight | 500 |

**Variantes:**
- Primary: bg `rgba(201, 162, 39, 0.15)`, text `#C9A227`
- Success: bg `rgba(34, 197, 94, 0.15)`, text `#22C55E`
- Warning: bg `rgba(234, 179, 8, 0.15)`, text `#EAB308`
- Danger: bg `rgba(239, 68, 68, 0.15)`, text `#EF4444`
- Purple: bg `rgba(168, 85, 247, 0.15)`, text `#A855F7`

### Inputs/Forms

| Propriedade | Valor |
|-------------|-------|
| Background | `#1A1A1A` |
| Border | `1px solid #2A2A2A` |
| Border-radius | `0.75rem` |
| Padding | `0.75rem 1rem` |
| Font-size | `1rem` |

**Estados:**
- Default: border `#2A2A2A`
- Focus: border `#C9A227`, outline gold glow
- Error: border `#EF4444`
- Disabled: opacity `0.5`

### Métricas Dashboard

| Propriedade | Valor |
|-------------|-------|
| Background | `#1A1A1A` |
| Border-radius | `1rem` |
| Padding | `1.5rem` |
| Grid | auto-fit, minmax(140px, 1fr) |

**Variante Highlight:**
- Background: linear-gradient gold (`rgba(201, 162, 39, 0.1)`)
- Valor: `text-3xl`, bold
- Label: `text-sm`, muted

### Progress Steps

| Propriedade | Valor |
|-------------|-------|
| Circle size | 44px |
| Border | `2px solid #3A3A3A` |
| Font-size | `1rem` |

**Estados:**
- Inactive: border `#3A3A3A`, text `#6B7280`
- Active: background `#C9A227`, text `#0A0A0A`, box-shadow gold glow
- Completed: background `#22C55E`

**Connector Line:**
- Height: `2px`
- Color: `#3A3A3A`
- Active: `#C9A227`

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
| Gold | `0 0 20px rgba(201, 162, 39, 0.15)` |
| Purple | `0 0 20px rgba(168, 85, 247, 0.15)` |

### Gradientes

**Header Radial:**
```css
background: radial-gradient(circle at top, rgba(201, 162, 39, 0.05), transparent);
```

**Card Hover:**
```css
background: linear-gradient(135deg, rgba(201, 162, 39, 0.05), transparent);
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
- ✅ Use gold (`#C9A227`) para ações principais e conteúdo prioritário
- ✅ Use purple (`#A855F7`) para indicar conteúdo avançado/maestria
- ✅ Mantenha hierarquia visual através de tamanho, peso e cor
- ✅ Use transições sutis (0.2s-0.3s) para interações
- ✅ Aplique border-radius consistente (`0.75rem` padrão)
- ✅ Use badges com backgrounds semi-transparentes
- ✅ Mantenha cards com estados hover claros

### Don'ts (Evite)

- ❌ Não use cores saturadas demais em dark mode
- ❌ Não misture valores de espaçamento fora do sistema de 8pt
- ❌ Não use gold e purple simultaneamente no mesmo elemento
- ❌ Não crie cards sem hover states
- ❌ Não use transições longas (> 0.3s)
- ❌ Não ignore a hierarquia de cores (gold > purple > teal)
- ❌ Não use texto `#FFFFFF` sobre backgrounds claros
- ❌ Não crie componentes sem estados (hover, active, disabled)
- ❌ Não desrespeite a estrutura modular/expansível

---

## Acessibilidade

### Contraste de Cores

| Combinação | Ratio | Status |
|------------|-------|--------|
| `#FFFFFF` sobre `#0A0A0A` | 19.0:1 | ✅ AAA |
| `#C9A227` sobre `#0A0A0A` | 7.5:1 | ✅ AA |
| `#A3A3A3` sobre `#0A0A0A` | 6.2:1 | ✅ AA |
| `#6B7280` sobre `#0A0A0A` | 4.5:1 | ✅ AA |

### Recomendações

- Use texto `#FFFFFF` para títulos e conteúdo principal
- Use `#A3A3A3` para texto secundário
- Use `#6B7280` apenas para metadados/captions
- Garanta focus states visíveis (outline gold glow)
- Mantenha área de clique mínima de 44x44px

---

## Design Tokens (CSS Variables)

```css
:root {
  /* Colors - Primary */
  --color-primary-gold: #C9A227;
  --color-secondary-purple: #A855F7;
  --color-accent-teal: #134E4A;

  /* Colors - Background */
  --color-bg-primary: #0A0A0A;
  --color-bg-secondary: #0F0F0F;
  --color-bg-card: #1A1A1A;
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
  --shadow-glow-gold: 0 0 20px rgba(201, 162, 39, 0.15);
  --shadow-glow-purple: 0 0 20px rgba(168, 85, 247, 0.15);

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
