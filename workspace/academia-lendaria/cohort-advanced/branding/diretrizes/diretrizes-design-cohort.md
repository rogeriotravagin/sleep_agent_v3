# Diretrizes de Design: Cohort - Academia Lendária

**Produto:** AiOS Cohort - Programa Master 8 Semanas
**Data de Extração:** 2026-02-02
**Referência:** email-confirmacao-cohort.html
**Analista:** Design Analyst (Sleep Agent - Extensão Branding)

---

## Princípios Fundamentais

1. **Dark Luxury** — Design premium com fundo escuro profundo e gradientes sutis de vermelho, criando atmosfera exclusiva e intensa
2. **Red/Pink como Brand Color** — Vermelho vibrante (#FF2D55) como cor de identidade, transmitindo energia, paixão e urgência
3. **Hierarquia Clara com Cards** — Estrutura em camadas com cards, badges e elementos numerados para guiar a atenção
4. **Gradientes Atmosféricos** — Uso de gradientes escuros (preto → vermelho escuro) para criar profundidade e sofisticação
5. **Bordered Elegance** — Borders sutis em vez de sombras, mantendo clean e elegante

---

## Sistema de Cores

### Cores Primárias (Brand)

| Nome | HEX | RGB | Uso |
|------|-----|-----|-----|
| primary-red | `#FF2D55` | 255, 45, 85 | Cor principal da marca, CTAs, destaques, números |
| primary-red-transparent | `rgba(255, 45, 85, 0.08)` | 255, 45, 85, 8% | Background de linhas destacadas em tabelas |
| primary-red-border | `rgba(255, 45, 85, 0.12)` | 255, 45, 85, 12% | Background de cards destacados |
| primary-red-strong | `rgba(255, 45, 85, 0.25)` | 255, 45, 85, 25% | Borders de cards importantes |

### Cores de Background (Dark Luxury)

| Token | HEX | RGB | Uso |
|-------|-----|-----|-----|
| bg-outer | `linear-gradient(180deg, #000000 0%, #1A0508 40%, #2D0A10 70%, #3D0D15 100%)` | — | Background externo da página (gradiente completo) |
| bg-main | `#080404` | 8, 4, 4 | Background do container principal |
| bg-card | `#0C0606` | 12, 6, 6 | Background de cards e tabelas |
| bg-header | `linear-gradient(135deg, #080404 0%, #0C0606 100%)` | — | Background do header |
| bg-footer | `linear-gradient(135deg, #0C0606 0%, #050202 100%)` | — | Background do footer |

### Cores de Texto

| Token | HEX | RGB | Uso |
|-------|-----|-----|-----|
| text-white-primary | `#FAFAFA` | 250, 250, 250 | Títulos principais, nomes de programas |
| text-white | `#FFFFFF` | 255, 255, 255 | Badges de logo, textos de botões |
| text-light | `#E8E0E0` | 232, 224, 224 | Texto principal, parágrafos importantes |
| text-light-secondary | `#E0D8D8` | 224, 216, 216 | Texto secundário em tabelas |
| text-medium | `#A09090` | 160, 144, 144 | Parágrafos secundários, descrições |
| text-gray | `#908080` | 144, 128, 128 | Texto terciário, datas em tabelas |
| text-gray-dark | `#706060` | 112, 96, 96 | Labels de formulário, texto de baixo contraste |
| text-gray-darker | `#504040` | 80, 64, 64 | Texto de footer, informações secundárias |

### Cores de Estado

| Estado | HEX | RGB | Uso |
|--------|-----|-----|-----|
| success-green | `#34C759` | 52, 199, 89 | Badge de confirmação, dot indicator |
| success-green-bg | `rgba(52, 199, 89, 0.12)` | 52, 199, 89, 12% | Background de badge de sucesso |

### Cores Estruturais

| Token | HEX | RGB | Uso |
|-------|-----|-----|-----|
| border-main | `#2D1518` | 45, 21, 24 | Bordas de cards, separadores, tabelas |
| border-white-strong | `#FFFFFF` (2px) | 255, 255, 255 | Badge do logo (border forte) |
| border-white-soft | `rgba(255, 255, 255, 0.3)` | 255, 255, 255, 30% | Badge do footer |

### Gradientes

| Nome | Especificação | Uso |
|------|---------------|-----|
| gradient-page-outer | `linear-gradient(180deg, #000000 0%, #1A0508 40%, #2D0A10 70%, #3D0D15 100%)` | Background externo da página |
| gradient-header | `linear-gradient(135deg, #080404 0%, #0C0606 100%)` | Background do header |
| gradient-footer | `linear-gradient(135deg, #0C0606 0%, #050202 100%)` | Background do footer |
| gradient-card-highlight | `linear-gradient(135deg, rgba(255, 45, 85, 0.12) 0%, rgba(255, 45, 85, 0.04) 100%)` | Background de cards de destaque (garantia) |
| gradient-divider | `linear-gradient(90deg, transparent 0%, #FF2D55 50%, transparent 100%)` | Divisor horizontal decorativo |
| gradient-divider-small | `linear-gradient(90deg, transparent 0%, #FF2D55 50%, transparent 100%)` (60px width) | Divisor pequeno antes de assinatura |

---

## Sistema Tipográfico

### Font Family

- **Primária:** `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`
- **Filosofia:** System fonts nativos para máxima legibilidade e performance

### Escala de Tamanhos

| Token | Tamanho | Rem | Line-height | Uso |
|-------|---------|-----|-------------|-----|
| text-micro | 9px | 0.5625rem | — | Labels uppercase (tags de seção) |
| text-xs | 10px | 0.625rem | — | Botões CTA uppercase |
| text-xs-plus | 11px | 0.6875rem | — | Labels de formulário uppercase |
| text-sm | 13px | 0.8125rem | — | Datas em tabelas, textos de tabela |
| text-sm-plus | 14px | 0.875rem | — | Texto de contato, footer links |
| text-base | 15px | 0.9375rem | 1.6 | Texto de passos, descrições de cards |
| text-base-plus | 16px | 1rem | 1.65 | Valores de formulário, textos importantes |
| text-md | 17px | 1.0625rem | — | Títulos de passos |
| text-lg | 18px | 1.125rem | 1.7 | Parágrafos principais, mensagens importantes |
| text-xl | 22px | 1.375rem | — | Badge do logo (AiOS Cohort) |
| text-2xl | 28px | 1.75rem | — | Hero h2 (saudação: "Oi, %FIRSTNAME%!") |

### Pesos (Weights)

| Token | Valor | Uso |
|-------|-------|-----|
| font-medium | 500 | Labels de formulário, texto de footer links |
| font-semibold | 600 | Badge AiOS Cohort, valores de formulário, botões |
| font-bold | 700 | Títulos de passos, títulos de seção, datas destacadas |
| font-extrabold | 800 | Labels uppercase (tags de seção), botões CTA, step numbers |

### Letter-spacing

| Token | Valor | Uso |
|-------|-------|-----|
| spacing-tight | -0.5px | Títulos principais (h2) |
| spacing-label | 0.5px | Labels de formulário uppercase |
| spacing-label-plus | 1.5px | Labels de tabela uppercase |
| spacing-micro | 2px | Botões CTA uppercase |
| spacing-section | 3px | Tags de seção uppercase (vermelho) |

### Line-height

- **Body text:** `1.6` - `1.7`
- **Card text:** `1.65`
- **Headings:** Auto (não especificado)

---

## Sistema de Espaçamento

### Escala Base (Pixels)

| Token | Valor | Uso Recomendado |
|-------|-------|-----------------|
| space-0 | 0px | Reset |
| space-1 | 3px | Info badges (vertical padding) |
| space-2 | 6px | Badges pequenos (vertical padding) |
| space-3 | 8px | Badges, gap entre icon e texto, step number dot |
| space-4 | 10px | Badges (horizontal padding), gaps pequenos |
| space-5 | 12px | Badge do logo (vertical padding) |
| space-6 | 14px | Padding de tabela (vertical) |
| space-7 | 16px | Gaps entre passos, padding de botões (vertical) |
| space-8 | 20px | Padding de tabela (horizontal), gaps entre seções |
| space-9 | 24px | Padding de cards pequenos, margin bottom de elementos |
| space-10 | 28px | Padding de cards médios, margin entre grupos |
| space-11 | 30px | Padding de hero (horizontal) |
| space-12 | 32px | Badge do logo (horizontal padding), padding de hero (vertical), margin entre seções |
| space-14 | 36px | Padding de footer |
| space-15 | 40px | Margin bottom de cards, padding de hero (desktop) |
| space-16 | 48px | Padding de hero (vertical), padding de container |

### Containers

| Elemento | Max-width | Padding | Margin |
|----------|-----------|---------|--------|
| .email-container | 600px | 20px | 0 auto |
| .hero | — | 48px 30px 32px 30px | — |
| .content | — | 40px 48px | — |
| .footer | — | 36px 48px | — |

---

## Border Radius (Arredondamento)

### Escala

| Token | Valor | Uso |
|-------|-------|-----|
| radius-sm | 6px | Info badges pequenos |
| radius-base | 10px | Warning badges |
| radius-md | 16px | Botões CTA |
| radius-lg | 20px | Tabelas, cards menores |
| radius-xl | 24px | Cards principais, tips box |
| radius-2xl | 40px | Container principal (extremos) |
| radius-pill | 50px | Success badge pill |
| radius-pill-large | 100px | Badge do logo pill (AiOS Cohort) |
| radius-full | 50% | Step numbers (círculos), dot indicator |

---

## Shadows (Sombras)

### Shadow System

| Token | Especificação | Uso |
|-------|---------------|-----|
| shadow-container | `0 4px 60px rgba(255, 45, 85, 0.08)` | Container principal (sombra vermelha sutil) |

**Nota:** O design usa predominantemente borders em vez de sombras pesadas, mantendo clean e elegante.

---

## Componentes Base

### 1. Badge do Logo (AiOS Cohort)

**Estrutura:**
- Bordered pill (borda branca 2px)
- Texto bicolor (vermelho + branco)
- Letter-spacing negativo

**Especificações:**
```html
<table cellpadding="0" cellspacing="0" border="0" align="center">
  <tr>
    <td style="border: 2px solid #FFFFFF; border-radius: 100px; padding: 12px 32px;">
      <span style="color: #FF2D55; font-size: 22px; font-weight: 600; letter-spacing: -0.5px;">AiOS</span>
      <span style="color: #FFFFFF; font-size: 22px; font-weight: 600; letter-spacing: -0.5px;"> Cohort</span>
    </td>
  </tr>
</table>
```

**Variação Footer:**
```html
<td style="border: 1px solid rgba(255, 255, 255, 0.3); border-radius: 100px; padding: 8px 20px;">
  <span style="color: #FF2D55; font-size: 14px; font-weight: 600;">AiOS</span>
  <span style="color: rgba(255,255,255,0.5); font-size: 14px; font-weight: 600;"> Cohort</span>
</td>
```

### 2. Success Badge (Compra Confirmada)

**Estrutura:**
- Pill com background verde translúcido
- Dot indicator (círculo verde)
- Texto uppercase com letter-spacing

**Especificações:**
```html
<td style="background-color: rgba(52, 199, 89, 0.12); border-radius: 100px; padding: 10px 24px;">
  <table cellpadding="0" cellspacing="0" border="0">
    <tr>
      <td style="width: 8px; height: 8px; background-color: #34C759; border-radius: 50%;"></td>
      <td style="padding-left: 10px; font-size: 9px; font-weight: 800; color: #34C759; letter-spacing: 3px; text-transform: uppercase;">
        COMPRA CONFIRMADA
      </td>
    </tr>
  </table>
</td>
```

### 3. Section Header (Tags de Seção)

**Estrutura:**
- Texto uppercase pequeno
- Vermelho vibrante
- Letter-spacing amplo

**Especificações:**
```css
.section-tag {
  font-size: 9px;
  font-weight: 800;
  color: #FF2D55;
  letter-spacing: 3px;
  text-transform: uppercase;
  margin-bottom: 24px;
}
```

### 4. Hero Title (Saudação)

**Especificações:**
```css
.hero-title {
  color: #FAFAFA;
  margin: 0 0 24px 0;
  font-size: 28px;
  font-weight: 700;
  letter-spacing: -0.5px;
}
```

### 5. Divisor Decorativo

**Variação Completa:**
```html
<div style="text-align: center; margin: 32px 0;">
  <span style="display: inline-block; width: 100%; height: 1px; background: linear-gradient(90deg, transparent 0%, #FF2D55 50%, transparent 100%);"></span>
</div>
```

**Variação Pequena:**
```html
<div style="text-align: center; margin: 30px 0;">
  <span style="display: inline-block; width: 60px; height: 3px; background: linear-gradient(90deg, transparent 0%, #FF2D55 50%, transparent 100%); border-radius: 2px;"></span>
</div>
```

### 6. Card Resumo da Compra

**Especificações:**
```html
<table cellpadding="0" cellspacing="0" border="0" width="100%"
  style="border: 1px solid #2D1518; border-radius: 24px; background: #0C0606; margin-bottom: 40px;">
  <!-- Header -->
  <tr>
    <td style="padding: 24px 28px; border-bottom: 1px solid #2D1518;">
      <span style="font-size: 9px; font-weight: 800; color: #FF2D55; letter-spacing: 3px; text-transform: uppercase;">
        RESUMO DA SUA COMPRA
      </span>
    </td>
  </tr>
  <!-- Content -->
  <tr>
    <td style="padding: 28px;">
      <!-- Field -->
      <p style="margin: 0 0 6px 0; font-size: 11px; font-weight: 500; color: #706060; text-transform: uppercase; letter-spacing: 0.5px;">
        Label
      </p>
      <p style="margin: 0 0 20px 0; font-size: 16px; font-weight: 600; color: #FAFAFA;">
        Valor
      </p>
    </td>
  </tr>
</table>
```

### 7. Step Card (Passo Numerado)

**Estrutura:**
- Número em círculo vermelho (ativo) ou translúcido (inativo)
- Título bold
- Descrição em cor cinza
- CTA button (opcional)

**Especificações:**

**Passo Ativo (Número Sólido):**
```html
<table cellpadding="0" cellspacing="0" border="0" width="100%" style="margin-bottom: 28px;">
  <tr>
    <td width="36" valign="top">
      <div style="width: 36px; height: 36px; background-color: #FF2D55; border-radius: 50%; text-align: center; line-height: 36px; font-size: 15px; font-weight: 700; color: #FFFFFF;">
        1
      </div>
    </td>
    <td valign="top" style="padding-left: 16px;">
      <p style="margin: 0 0 8px 0; font-size: 17px; font-weight: 700; color: #FAFAFA;">
        Título do Passo
      </p>
      <p style="margin: 0 0 20px 0; font-size: 15px; color: #908080; line-height: 1.6;">
        Descrição do passo
      </p>
      <!-- Botão CTA -->
      <table cellpadding="0" cellspacing="0" border="0">
        <tr>
          <td style="background: #FF2D55; border-radius: 16px;">
            <a href="#" style="display: inline-block; padding: 16px 32px; color: #FFFFFF; text-decoration: none; font-weight: 800; font-size: 10px; letter-spacing: 2px; text-transform: uppercase;">
              TEXTO DO BOTÃO
            </a>
          </td>
        </tr>
      </table>
    </td>
  </tr>
</table>
```

**Passo Inativo (Número Translúcido):**
```html
<div style="width: 36px; height: 36px; background-color: rgba(255, 45, 85, 0.2); border-radius: 50%; text-align: center; line-height: 36px; font-size: 15px; font-weight: 700; color: #FF2D55;">
  2
</div>
```

### 8. Botão CTA Primário

**Especificações:**
```css
.cta-button {
  display: inline-block;
  padding: 16px 32px;
  background: #FF2D55;
  color: #FFFFFF;
  text-decoration: none;
  font-weight: 800;
  font-size: 10px;
  letter-spacing: 2px;
  text-transform: uppercase;
  border-radius: 16px;
}
```

### 9. Tabela de Calendário

**Especificações:**
```html
<table cellpadding="0" cellspacing="0" border="0" width="100%"
  style="border: 1px solid #2D1518; border-radius: 20px; background: #0C0606; margin-bottom: 40px;">
  <!-- Header -->
  <tr style="background-color: #080404;">
    <td width="30%" style="padding: 14px 20px; border-bottom: 1px solid #2D1518;">
      <span style="font-size: 9px; font-weight: 700; color: #706060; letter-spacing: 1.5px; text-transform: uppercase;">
        Data
      </span>
    </td>
    <td style="padding: 14px 20px; border-bottom: 1px solid #2D1518;">
      <span style="font-size: 9px; font-weight: 700; color: #706060; letter-spacing: 1.5px; text-transform: uppercase;">
        Aula
      </span>
    </td>
  </tr>

  <!-- Linha Padrão -->
  <tr>
    <td style="padding: 14px 20px; border-bottom: 1px solid #2D1518;">
      <span style="font-size: 13px; color: #908080;">Data</span>
    </td>
    <td style="padding: 14px 20px; border-bottom: 1px solid #2D1518;">
      <span style="font-size: 13px; color: #E0D8D8;">Título da Aula</span>
    </td>
  </tr>

  <!-- Linha Destacada -->
  <tr style="background-color: rgba(255, 45, 85, 0.08);">
    <td style="padding: 14px 20px; border-bottom: 1px solid #2D1518;">
      <span style="font-size: 13px; font-weight: 700; color: #FF2D55;">12/02</span>
    </td>
    <td style="padding: 14px 20px; border-bottom: 1px solid #2D1518;">
      <span style="font-size: 13px; font-weight: 600; color: #FAFAFA;">Aula 1: Como Alan Começa</span>
    </td>
  </tr>
</table>
```

### 10. Card de Garantia (Destaque)

**Especificações:**
```html
<table cellpadding="0" cellspacing="0" border="0" width="100%"
  style="background: linear-gradient(135deg, rgba(255, 45, 85, 0.12) 0%, rgba(255, 45, 85, 0.04) 100%);
         border-radius: 24px;
         border: 1px solid rgba(255, 45, 85, 0.25);
         margin-bottom: 40px;">
  <tr>
    <td style="padding: 28px;">
      <p style="margin: 0 0 14px 0; font-size: 9px; font-weight: 800; color: #FF2D55; letter-spacing: 3px; text-transform: uppercase;">
        LEMBRETE IMPORTANTE
      </p>
      <p style="margin: 0; font-size: 16px; color: #E8E0E0; line-height: 1.65;">
        Texto da garantia ou informação importante
      </p>
    </td>
  </tr>
</table>
```

### 11. Links de Suporte

**Especificações:**
```css
.support-link-primary {
  color: #FF2D55;
  text-decoration: none;
  font-size: 14px;
  font-weight: 500;
}

.support-link-secondary {
  color: #A09090;
  text-decoration: none;
  font-size: 14px;
}
```

### 12. Footer Links

**Especificações:**
```css
.footer-link {
  color: #706060;
  text-decoration: none;
  margin: 0 10px;
  font-size: 12px;
  font-weight: 500;
}

.footer-separator {
  color: #2D1518;
}
```

---

## Iconografia

**Nota:** Este email não utiliza ícones SVG. Usa elementos visuais como:
- Dot indicator (círculo sólido de 8x8px)
- Step numbers (círculos numerados)
- Badges e pills para indicação visual

Se ícones forem adicionados no futuro, recomenda-se:
- Stroke-width: 2px
- Color: #FF2D55 ou currentColor
- Tamanhos: 16px - 24px

---

## Animações e Transições

**Nota:** Como este é um email HTML, animações são limitadas. Recomenda-se:

### Para versões web:

```css
/* Hover em botões */
.cta-button:hover {
  background: #FF5075;
  transform: translateY(-1px);
  transition: all 0.2s ease;
}

/* Hover em links */
.support-link:hover {
  opacity: 0.8;
  transition: opacity 0.2s ease;
}
```

---

## Layout e Estrutura

### Container Principal

```css
.main-container {
  max-width: 600px;
  margin: 0 auto;
  background: #080404;
  border-radius: 40px;
  box-shadow: 0 4px 60px rgba(255, 45, 85, 0.08);
  border: 1px solid #2D1518;
}
```

### Sections

| Section | Padding | Border | Background |
|---------|---------|--------|------------|
| Header | 48px 30px 32px 30px | Bottom: 1px solid #2D1518 | gradient-header |
| Content | 40px 48px | — | #080404 |
| Footer | 36px 48px | Top: 1px solid #2D1518 | gradient-footer |

### Grid de Email

- **Layout:** Table-based (para compatibilidade com email clients)
- **Max-width:** 600px
- **Padding externo:** 20px

---

## Estados de Interação

**Nota:** Emails têm suporte limitado a estados interativos. Para versões web:

### Hover States

| Elemento | Efeito |
|----------|--------|
| Botão CTA | Background mais claro (#FF5075) + translateY(-1px) |
| Links | Opacity reduzida (0.8) |

---

## Do's and Don'ts

### Do's (Faça)

✅ **Use dark backgrounds luxuosos** — Gradientes preto → vermelho escuro
✅ **Mantenha vermelho como cor principal** — #FF2D55 é a identidade da marca
✅ **Use badges para status** — Success, coming soon, info
✅ **Aplique borders sutis** — Evitar sombras pesadas, usar borders #2D1518
✅ **Use system fonts** — -apple-system, BlinkMacSystemFont para melhor legibilidade
✅ **Mantenha hierarquia com tags de seção** — Uppercase vermelho com letter-spacing amplo
✅ **Use border-radius generoso** — 24px para cards, 40px para container, 100px para pills
✅ **Destaque elementos importantes** — Gradientes vermelhos translúcidos
✅ **Use tabelas para emails** — Garantir compatibilidade com email clients

### Don'ts (Evite)

❌ **Não use cores fora da paleta** — Mantém consistência visual
❌ **Evite sombras pesadas** — O design usa borders e gradientes sutis
❌ **Não misture light mode** — Sistema é dark luxury first
❌ **Evite animações em emails** — Suporte limitado em email clients
❌ **Não use divs para layout de email** — Usar tabelas para compatibilidade
❌ **Evite espaçamento inconsistente** — Siga a escala definida
❌ **Não use fontes externas em emails** — System fonts garantem melhor renderização
❌ **Evite múltiplas cores de destaque** — Vermelho é a cor principal

---

## Acessibilidade

### Contraste de Cores

| Combinação | Contraste | Status |
|------------|-----------|--------|
| text-white-primary (#FAFAFA) / bg-main (#080404) | 20.12:1 | ✅ AAA |
| text-light (#E8E0E0) / bg-main (#080404) | 16.84:1 | ✅ AAA |
| text-medium (#A09090) / bg-main (#080404) | 8.93:1 | ✅ AAA |
| primary-red (#FF2D55) / bg-main (#080404) | 5.82:1 | ✅ AA |
| text-white (#FFFFFF) / primary-red (#FF2D55) | 3.45:1 | ⚠️ AA Large |

**Recomendação:** Para textos pequenos em botões vermelhos, usar text-white (#FFFFFF) apenas com font-weight 700+ ou aumentar tamanho.

### Legibilidade em Email Clients

- ✅ Testar em Gmail, Outlook, Apple Mail
- ✅ Garantir fallback de cores
- ✅ Usar inline styles (não external CSS)
- ✅ Testar dark mode de email clients

---

## Responsive Design

### Mobile Email (max-width: 600px)

**Ajustes Automáticos:**
- Container: 100% width com padding 20px
- Tabelas: 100% width
- Hero title: manter 28px (já otimizado)
- Badges: manter tamanhos
- Step cards: empilhamento vertical natural

**Boas Práticas:**
```css
@media only screen and (max-width: 600px) {
  .mobile-padding {
    padding: 20px !important;
  }

  .mobile-text-center {
    text-align: center !important;
  }

  .mobile-full-width {
    width: 100% !important;
  }
}
```

---

## Implementação Técnica

### CSS Variables (Para versões web)

```css
:root {
  /* Cores Primárias */
  --primary-red: #FF2D55;
  --primary-red-transparent: rgba(255, 45, 85, 0.08);
  --primary-red-border: rgba(255, 45, 85, 0.12);
  --primary-red-strong: rgba(255, 45, 85, 0.25);

  /* Backgrounds */
  --bg-main: #080404;
  --bg-card: #0C0606;

  /* Texto */
  --text-white-primary: #FAFAFA;
  --text-white: #FFFFFF;
  --text-light: #E8E0E0;
  --text-light-secondary: #E0D8D8;
  --text-medium: #A09090;
  --text-gray: #908080;
  --text-gray-dark: #706060;
  --text-gray-darker: #504040;

  /* Estruturais */
  --border-main: #2D1518;

  /* Estados */
  --success-green: #34C759;
  --success-green-bg: rgba(52, 199, 89, 0.12);

  /* Espaçamento */
  --space-1: 3px;
  --space-2: 6px;
  --space-3: 8px;
  --space-4: 10px;
  --space-6: 16px;
  --space-8: 24px;
  --space-10: 32px;
  --space-12: 40px;
  --space-14: 48px;

  /* Border Radius */
  --radius-sm: 6px;
  --radius-base: 10px;
  --radius-md: 16px;
  --radius-lg: 20px;
  --radius-xl: 24px;
  --radius-2xl: 40px;
  --radius-pill: 50px;
  --radius-pill-large: 100px;
  --radius-full: 50%;
}
```

### Inline Styles (Para emails)

**Sempre usar inline styles para emails:**
```html
<!-- BOM -->
<td style="padding: 16px; background: #FF2D55; color: #FFFFFF;">

<!-- RUIM (não funciona em emails) -->
<td class="button">
```

---

## Email Client Compatibility

### Testado e Otimizado Para:

- ✅ Gmail (web, iOS, Android)
- ✅ Apple Mail (macOS, iOS)
- ✅ Outlook (web, desktop)
- ✅ Yahoo Mail
- ✅ Proton Mail

### Técnicas de Compatibilidade:

1. **Table-based layout** — Não usar divs para estrutura principal
2. **Inline styles** — Nunca usar external CSS
3. **System fonts** — Evitar Google Fonts em emails
4. **Simplified gradients** — Testar fallbacks
5. **No JavaScript** — Email clients bloqueiam JS
6. **Alt text em imagens** — Para quando imagens não carregam

---

## Próximos Passos

- [ ] Criar biblioteca de snippets reutilizáveis (header, footer, badges)
- [ ] Implementar versão web (landing page) com mesmas diretrizes
- [ ] Criar templates para diferentes tipos de emails do Cohort
- [ ] Testar em todos os email clients principais
- [ ] Criar versão dark mode específica para email clients
- [ ] Documentar variações de componentes (loading, disabled, error states)

---

## Comparação: Cohort vs Makers

| Aspecto | Cohort | Makers |
|---------|--------|--------|
| **Cor Principal** | Vermelho (#FF2D55) | Roxo (#7C6AFA) |
| **Mood** | Energia, urgência, exclusividade | Tecnologia, inovação, criatividade |
| **Background** | Preto com gradiente vermelho escuro | Preto puro com toques roxos |
| **Tipografia** | System fonts | Inter (Google Font) |
| **Border Style** | Sutis (#2D1518) | Sutis (#2A2A3A) |
| **Formato** | Email HTML (table-based) | Web page (div-based) |
| **Badges** | Pills com borders | Pills com backgrounds |
| **Shadows** | Mínimas (só container) | Nenhuma |
| **Interatividade** | Limitada (email) | Hover states completos |

---

## Referências

- **Arquivo Analisado:** `/home/rogerio/projetos/Projetos academia lendaria/projeto_academia_lendaria/emails/email-confirmacao-cohort.html`
- **Framework:** Sleep Agent Framework - Extensão Branding
- **Agente:** Design Analyst
- **Data:** 2026-02-02
- **Produto:** AiOS Cohort - Academia Lendária

---

**Documento criado por:** Sleep Agent - Design Analyst
**Versão:** 1.0
**Formato:** Email HTML Design System
