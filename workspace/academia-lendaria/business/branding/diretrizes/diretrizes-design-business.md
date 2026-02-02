# Diretrizes de Design - Business Lendários

> **Produto:** Business Lendários
> **Versão:** 1.0
> **Última atualização:** 2026-02-02
> **Referência:** business-lendaria2.html

---

## 1. Identidade Visual

### 1.1 Paleta de Cores

#### Cores Principais

| Nome | Hex | RGB | Uso |
|------|-----|-----|-----|
| **Primary Cyan** | `#32ADE6` | rgb(50, 173, 230) | Elementos principais, CTAs, destaques |
| **Primary Cyan Light** | `#5BC0EB` | rgb(91, 192, 235) | Hover states, gradientes, ícones |
| **Primary Cyan Dark** | `#1A8DC7` | rgb(26, 141, 199) | Gradientes, sombras, variações |

#### Cores de Fundo

| Nome | Hex | RGB | Uso |
|------|-----|-----|-----|
| **BG Dark** | `#0A0A12` | rgb(10, 10, 18) | Background principal do body |
| **BG Card** | `#12121C` | rgb(18, 18, 28) | Cards, containers |
| **BG Card Hover** | `#1A1A28` | rgb(26, 26, 40) | Estado hover de cards |

#### Cores de Texto

| Nome | Hex | RGB | Uso |
|------|-----|-----|-----|
| **Text White** | `#FFFFFF` | rgb(255, 255, 255) | Títulos principais, texto de destaque |
| **Text Gray Light** | `#C0C0D0` | rgb(192, 192, 208) | Descrições, parágrafos |
| **Text Gray** | `#A0A0B0` | rgb(160, 160, 176) | Textos secundários |

#### Cores Funcionais

| Nome | Hex | RGB | Uso |
|------|-----|-----|-----|
| **Border Color** | `#252535` | rgb(37, 37, 53) | Bordas, separadores |
| **Success Green** | `#4ADE80` | rgb(74, 222, 128) | Indicadores de sucesso, tags positivas |
| **Warning Orange** | `#FB923C` | rgb(251, 146, 60) | "Em breve", alertas, avisos |

### 1.2 Gradientes

#### Background Principal
```css
background: linear-gradient(180deg, #0A0A12 0%, #080810 100%);
```

#### Hero Section
```css
background: linear-gradient(135deg, rgba(50, 173, 230, 0.1) 0%, rgba(50, 173, 230, 0.03) 100%);
```

#### Título Hero (Text Gradient)
```css
background: linear-gradient(135deg, #FFFFFF 0%, #5BC0EB 100%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
```

#### Produto Principal (Card)
```css
background: linear-gradient(135deg, rgba(50, 173, 230, 0.15) 0%, rgba(50, 173, 230, 0.05) 100%);
```

#### Ícones de Seção
```css
background: linear-gradient(135deg, #32ADE6 0%, #1A8DC7 100%);
```

#### Efeito Radial (Hero)
```css
background: radial-gradient(circle at center, rgba(50, 173, 230, 0.1) 0%, transparent 50%);
```

---

## 2. Tipografia

### 2.1 Fonte Principal

```css
font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
```

**Google Fonts:**
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
```

### 2.2 Escala Tipográfica

| Elemento | Tamanho | Peso | Uso |
|----------|---------|------|-----|
| **Hero H1** | 2.5rem (40px) | 800 | Título principal da página |
| **Hero P** | 1.1rem (17.6px) | 400 | Subtítulo hero |
| **Section Title** | 1.5rem (24px) | 700 | Títulos de seção |
| **Main Product Title** | 1.5rem (24px) | 700 | Produto em destaque |
| **Card Title** | 1.1rem (17.6px) | 600 | Títulos de cards |
| **Step Title** | 1.1rem (17.6px) | 600 | Títulos de passos |
| **Body** | 1rem (16px) | 400 | Texto padrão |
| **Card Description** | 0.95rem (15.2px) | 400 | Descrições |
| **Small Text** | 0.9rem (14.4px) | 500 | Links, botões |
| **Badges** | 0.75rem (12px) | 700 | Badges, tags |

### 2.3 Line Height

```css
line-height: 1.6; /* Padrão para body */
line-height: 1.7; /* Descrições longas */
```

---

## 3. Espaçamento

### 3.1 Sistema de Espaçamento

| Valor | Uso |
|-------|-----|
| **4px** | Espaçamento mínimo entre elementos inline |
| **6px** | Gaps pequenos, padding de tags |
| **8px** | Gaps em badges, ícones |
| **12px** | Gaps médios, padding de elementos |
| **16px** | Margin bottom padrão de parágrafos |
| **20px** | Padding de seções |
| **24px** | Padding de cards, margin entre seções |
| **32px** | Padding de produtos principais |
| **40px** | Margin entre seções principais |
| **60px** | Padding vertical de hero |

### 3.2 Container

```css
max-width: 800px;
margin: 0 auto;
padding: 40px 24px;
```

---

## 4. Border Radius

### 4.1 Escala de Arredondamento

| Valor | Uso |
|-------|-----|
| **6px** | Tags pequenas, badges menores |
| **10px** | Botões de ação |
| **12px** | Ícones, badges médios |
| **16px** | Cards padrão, containers |
| **20px** | Cards principais, containers grandes |
| **24px** | Hero sections |
| **50px** | Badges arredondados, pills |

---

## 5. Componentes

### 5.1 Hero Section

**Estrutura:**
```css
padding: 60px 20px;
background: linear-gradient(135deg, rgba(50, 173, 230, 0.1) 0%, rgba(50, 173, 230, 0.03) 100%);
border-radius: 24px;
border: 1px solid rgba(50, 173, 230, 0.25);
```

**Badge Hero:**
```css
background: #32ADE6;
color: white;
padding: 8px 16px;
border-radius: 50px;
font-size: 14px;
font-weight: 600;
```

**Efeito Pulse:**
```css
animation: pulse 4s ease-in-out infinite;

@keyframes pulse {
    0%, 100% { transform: scale(1); opacity: 0.5; }
    50% { transform: scale(1.1); opacity: 0.8; }
}
```

### 5.2 Cards

**Card Padrão:**
```css
background: #12121C;
border: 1px solid #252535;
border-radius: 16px;
padding: 24px;
transition: all 0.3s ease;
```

**Card Hover:**
```css
background: #1A1A28;
border-color: rgba(50, 173, 230, 0.5);
transform: translateY(-2px);
```

**Card Principal (Destaque):**
```css
background: linear-gradient(135deg, rgba(50, 173, 230, 0.15) 0%, rgba(50, 173, 230, 0.05) 100%);
border: 2px solid #32ADE6;
border-radius: 20px;
padding: 32px;
```

### 5.3 Botões

**Botão Primário:**
```css
background: #32ADE6;
color: white;
padding: 10px 20px;
border-radius: 10px;
font-weight: 600;
font-size: 0.9rem;
transition: all 0.2s ease;
```

**Botão Hover:**
```css
background: #5BC0EB;
transform: translateY(-1px);
```

**Botão com Ícone:**
```css
display: inline-flex;
align-items: center;
gap: 8px;
```

### 5.4 Badges & Tags

**Badge Produto Principal:**
```css
background: #32ADE6;
color: white;
padding: 6px 12px;
border-radius: 6px;
font-size: 0.75rem;
font-weight: 700;
text-transform: uppercase;
letter-spacing: 0.5px;
```

**Badge "Em Breve":**
```css
background: rgba(251, 146, 60, 0.2);
color: #FB923C;
padding: 10px 16px;
border-radius: 10px;
font-size: 0.9rem;
```

**Tag Sucesso:**
```css
background: rgba(74, 222, 128, 0.15);
color: #4ADE80;
padding: 4px 10px;
border-radius: 6px;
font-size: 0.8rem;
font-weight: 500;
```

**Tag Frequência:**
```css
background: rgba(50, 173, 230, 0.2);
color: #5BC0EB;
padding: 4px 10px;
border-radius: 6px;
font-size: 0.8rem;
font-weight: 600;
```

### 5.5 Ícones

**Ícone de Seção:**
```css
width: 40px;
height: 40px;
background: linear-gradient(135deg, #32ADE6 0%, #1A8DC7 100%);
border-radius: 12px;
display: flex;
align-items: center;
justify-content: center;
```

**Ícone SVG:**
```css
width: 20px;
height: 20px;
color: white;
```

**Ícone de Feature:**
```css
width: 24px;
height: 24px;
background: rgba(50, 173, 230, 0.2);
border-radius: 6px;
```

### 5.6 Steps (Passos)

**Step Card:**
```css
background: #12121C;
border: 1px solid #252535;
border-radius: 16px;
padding: 24px;
display: flex;
gap: 20px;
```

**Step Number:**
```css
width: 48px;
height: 48px;
background: linear-gradient(135deg, #32ADE6 0%, #1A8DC7 100%);
border-radius: 12px;
font-size: 1.3rem;
font-weight: 800;
```

### 5.7 Tabela de Comparação

```css
width: 100%;
border-collapse: separate;
border-spacing: 0;
border-radius: 16px;
border: 1px solid #252535;

/* Header */
th {
    background: #32ADE6;
    color: white;
    font-weight: 600;
    padding: 16px 20px;
}

/* Células */
td {
    background: #12121C;
    padding: 16px 20px;
    border-bottom: 1px solid #252535;
}
```

### 5.8 Tips Box

```css
background: linear-gradient(135deg, rgba(50, 173, 230, 0.1) 0%, rgba(50, 173, 230, 0.03) 100%);
border: 1px solid rgba(50, 173, 230, 0.3);
border-radius: 16px;
padding: 24px;
```

### 5.9 Links

**Link Padrão:**
```css
color: #5BC0EB;
text-decoration: none;
font-weight: 500;
display: inline-flex;
align-items: center;
gap: 6px;
transition: gap 0.2s ease;
```

**Link Hover:**
```css
gap: 10px; /* Aumenta o gap no hover */
```

---

## 6. Bordas

### 6.1 Padrões de Borda

**Borda Padrão:**
```css
border: 1px solid #252535;
```

**Borda com Destaque:**
```css
border: 1px solid rgba(50, 173, 230, 0.25);
```

**Borda Principal:**
```css
border: 2px solid #32ADE6;
```

**Borda Hover:**
```css
border-color: rgba(50, 173, 230, 0.5);
```

**Border Bottom (Separadores):**
```css
border-bottom: 1px solid #252535;
padding-bottom: 12px;
```

**Border Left (Quote/Destaque):**
```css
border-left: 3px solid #252535;
padding-left: 12px;
```

---

## 7. Efeitos e Transições

### 7.1 Transições

**Transição Padrão:**
```css
transition: all 0.3s ease;
```

**Transição de Botão:**
```css
transition: all 0.2s ease;
```

**Transição de Link:**
```css
transition: gap 0.2s ease;
```

### 7.2 Transforms

**Hover Cards:**
```css
transform: translateY(-2px);
```

**Hover Botões:**
```css
transform: translateY(-1px);
```

### 7.3 Animações

**Pulse (Hero Background):**
```css
animation: pulse 4s ease-in-out infinite;

@keyframes pulse {
    0%, 100% { transform: scale(1); opacity: 0.5; }
    50% { transform: scale(1.1); opacity: 0.8; }
}
```

**Spin (Loading/Em Breve):**
```css
animation: spin 2s linear infinite;

@keyframes spin {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
}
```

---

## 8. Grid e Layout

### 8.1 Card Grid

```css
display: grid;
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
gap: 16px;
```

### 8.2 Live Events Grid

```css
display: grid;
grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
gap: 16px;
```

### 8.3 Tips Grid

```css
display: grid;
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
gap: 12px;
```

---

## 9. Responsividade

### 9.1 Mobile (max-width: 600px)

**Hero H1:**
```css
font-size: 1.8rem; /* reduz de 2.5rem */
```

**Grid:**
```css
grid-template-columns: 1fr; /* força coluna única */
```

**Step Cards:**
```css
flex-direction: column;
align-items: stretch;
```

**Step Number:**
```css
width: 40px;
height: 40px;
font-size: 1.1rem;
```

**Tabela:**
```css
padding: 12px;
font-size: 0.9rem;
```

**Produto Principal:**
```css
padding: 24px; /* reduz de 32px */
```

---

## 10. Ícones SVG

### 10.1 Biblioteca de Ícones

Todos os ícones utilizam SVG inline com stroke (outline style).

**Configuração Padrão:**
```html
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
    <!-- paths aqui -->
</svg>
```

**Ícones Utilizados:**

- **Info Circle:** Seções informativas
- **Book:** Conteúdo educacional
- **Video:** Encontros ao vivo
- **Bar Chart:** Comparações
- **Star:** Dicas
- **Check:** Passos concluídos
- **Arrow Right:** Links e navegação
- **Dollar Sign:** Monetização
- **Check Circle:** Validação
- **Bell:** Notificações
- **Users:** Comunidade
- **Message:** Chat/WhatsApp
- **Monitor:** Plataforma
- **Code:** Mentorias técnicas
- **TrendingUp:** Negócios
- **Play Circle:** Onboarding
- **Infinity:** Logo/Brand
- **Lightning:** Destaque
- **Calendar:** Agendamento

---

## 11. Padrões de Conteúdo

### 11.1 Estrutura de Seção

```html
<div class="section">
    <div class="section-header">
        <div class="section-icon">[ícone]</div>
        <h2 class="section-title">Título</h2>
    </div>
    <div class="section-content">
        [conteúdo]
    </div>
</div>
```

### 11.2 Feature List

```html
<ul class="feature-list">
    <li>
        <div class="feature-icon">[ícone]</div>
        <div class="feature-text">
            <strong>Título da Feature</strong>
            <span>Descrição da feature</span>
        </div>
    </li>
</ul>
```

### 11.3 Card Padrão

```html
<div class="card">
    <div class="card-header">
        <svg class="card-icon">[ícone]</svg>
        <h3 class="card-title">Título</h3>
    </div>
    <p class="card-description">Descrição</p>
    <a href="#" class="card-link">
        Ação
        <svg>[ícone arrow]</svg>
    </a>
</div>
```

---

## 12. Acessibilidade

### 12.1 Contraste

Todas as combinações de cores seguem WCAG 2.1 AA:

- **Texto branco (#FFFFFF)** sobre **BG Dark (#0A0A12)**: ✓ Passar AA
- **Primary Cyan (#32ADE6)** sobre **BG Dark**: ✓ Passar AA
- **Text Gray Light (#C0C0D0)** sobre **BG Dark**: ✓ Passar AA

### 12.2 Estados Interativos

Todos os elementos interativos têm:
- Estado hover visível
- Cursor pointer
- Transições suaves

### 12.3 Semântica

- Uso correto de headings (h1, h2, h3)
- Links com texto descritivo
- Ícones com cores informativas

---

## 13. Performance

### 13.1 Otimizações CSS

- Use de `transform` para animações (melhor performance)
- `will-change` não é necessário (transições simples)
- Gradientes em CSS (não imagens)
- SVG inline para ícones (reduz requests)

### 13.2 Fontes

```css
font-display: swap; /* Já incluído no Google Fonts */
```

---

## 14. Checklist de Implementação

Ao criar novas páginas para Business Lendários, verifique:

- [ ] Paleta de cores correta (#32ADE6 como primary)
- [ ] Fonte Inter carregada do Google Fonts
- [ ] Background com gradiente escuro
- [ ] Border radius seguindo a escala (6px-50px)
- [ ] Cards com hover effect
- [ ] Transições suaves (0.2s-0.3s)
- [ ] Ícones SVG com stroke
- [ ] Badges e tags com cores funcionais
- [ ] Responsividade mobile (600px breakpoint)
- [ ] Contraste de texto adequado
- [ ] Container max-width 800px

---

## 15. Recursos

### 15.1 Ferramentas Recomendadas

- **Coolors.co**: Para visualizar paleta de cores
- **Google Fonts**: Inter font family
- **Heroicons**: Similar style para novos ícones SVG
- **Figma**: Para mockups e protótipos

### 15.2 Referências

- **Arquivo fonte:** `business-lendaria2.html`
- **Design System:** Este documento
- **Última revisão:** 2026-02-02

---

## 16. Notas Importantes

### 16.1 Tom Visual

O design transmite:
- **Profissionalismo**: Cores escuras, tipografia limpa
- **Inovação**: Gradientes cyan, efeitos modernos
- **Confiança**: Hierarquia clara, espaçamento generoso
- **Ação**: CTAs destacados, cores vibrantes

### 16.2 Diferencial

- **Dark Mode nativo**: Todo design já é dark
- **Cyan como identidade**: Diferenciação clara
- **Micro-interações**: Hovers e transições refinadas
- **Hierarquia visual forte**: Produtos principais em destaque

---

## Versionamento

| Versão | Data | Alterações |
|--------|------|------------|
| 1.0 | 2026-02-02 | Extração inicial das diretrizes da página business-lendaria2.html |

---

**Organizado por:** Sleep Agent
**Extensão:** Branding/Design
**Produto:** Business Lendários - Academia Lendária
