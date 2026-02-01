# Diretrizes de Design - Sleep Agent Marketing

## Visão Geral

Design moderno, minimalista e elegante com tema escuro (dark mode). Estilo premium que transmite sofisticação e profissionalismo.

---

## Paleta de Cores

### Cores Primárias

| Cor | Hex | Uso |
|-----|-----|-----|
| Roxo Escuro | `#1a1030` | Background principal |
| Púrpura Médio | `#4a2c6a` | Gradientes, destaques |
| Magenta Suave | `#8b5a8c` | Acentos, hover states |
| Rosa Suave | `#c4a0b0` | Highlights sutis |

### Cores Neutras

| Cor | Hex | Uso |
|-----|-----|-----|
| Branco | `#ffffff` | Texto principal, ícones |
| Branco Transparente | `rgba(255,255,255,0.7)` | Texto secundário |
| Branco Sutil | `rgba(255,255,255,0.3)` | Bordas, placeholders |

### Gradiente Principal

```css
background: linear-gradient(
  135deg,
  #1a1030 0%,
  #2d1f4a 25%,
  #4a2c6a 50%,
  #8b5a8c 75%,
  #c4a0b0 100%
);
```

---

## Tipografia

### Família de Fontes

```css
font-family: 'Inter', 'Helvetica Neue', Arial, sans-serif;
```

### Hierarquia

| Elemento | Tamanho | Peso | Estilo |
|----------|---------|------|--------|
| H1 (Hero) | 64px - 80px | 100 - 200 (Ultra Light) | Letter-spacing: 0.3em |
| H2 | 36px - 48px | 300 (Light) | Letter-spacing: 0.1em |
| Corpo | 14px - 16px | 400 (Regular) | Line-height: 1.7 |
| Navegação | 14px | 500 (Medium) | Uppercase opcional |
| Botões | 14px | 500 (Medium) | Letter-spacing: 0.05em |

### Características

- **Headlines**: Tipografia extremamente fina (thin/light)
- **Espaçamento**: Generoso entre letras em títulos
- **Alinhamento**: Centralizado no hero, esquerda em conteúdo

---

## Layout

### Estrutura da Página

```
┌─────────────────────────────────────────────┐
│  HEADER (fixo, transparente)                │
│  [Logo] [Busca] [Nav] [Nav] [Nav] [CTA]     │
├─────────────────────────────────────────────┤
│                                             │
│              HERO SECTION                   │
│           (viewport height)                 │
│                                             │
│              TÍTULO GRANDE                  │
│                                             │
│         Texto descritivo curto              │
│         centralizado (max 600px)            │
│                                             │
│            [ BOTÃO CTA ]                    │
│                                             │
└─────────────────────────────────────────────┘
```

### Espaçamentos

| Elemento | Valor |
|----------|-------|
| Padding container | 20px - 40px |
| Gap navegação | 32px - 48px |
| Margem entre elementos hero | 24px - 32px |
| Padding botões | 12px 32px |

### Larguras

- **Container máximo**: 1200px
- **Texto hero**: max-width 600px
- **Centralização**: margin 0 auto

---

## Componentes

### Header/Navegação

```css
.header {
  position: fixed;
  top: 0;
  width: 100%;
  padding: 20px 40px;
  background: transparent;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-link {
  color: rgba(255, 255, 255, 0.8);
  text-decoration: none;
  font-size: 14px;
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: #ffffff;
}
```

### Campo de Busca

```css
.search-box {
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 20px;
  padding: 8px 16px;
  color: white;
}

.search-box::placeholder {
  color: rgba(255, 255, 255, 0.5);
}
```

### Botão Primário (CTA)

```css
.btn-primary {
  background: transparent;
  border: 1px solid rgba(255, 255, 255, 0.5);
  border-radius: 25px;
  padding: 12px 32px;
  color: white;
  font-size: 14px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn-primary:hover {
  background: rgba(255, 255, 255, 0.1);
  border-color: white;
}
```

### Botão Secundário (Join)

```css
.btn-secondary {
  background: rgba(255, 255, 255, 0.15);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 4px;
  padding: 8px 20px;
  color: white;
}
```

---

## Efeitos Visuais

### Gradiente de Fundo

- Usar gradientes suaves e fluidos
- Transições de cor naturais (não abruptas)
- Efeito "aurora" ou "nebulosa" opcional

### Blur e Transparência

```css
/* Glassmorphism sutil */
.glass-element {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.1);
}
```

### Transições

```css
/* Padrão para todos os elementos interativos */
transition: all 0.3s ease;
```

---

## Princípios de Design

### Do's (Fazer)

- Usar muito espaço em branco (respiro visual)
- Manter hierarquia clara
- Priorizar legibilidade
- Usar transparências sutis
- Animações suaves e elegantes

### Don'ts (Evitar)

- Texto pequeno demais sobre gradientes
- Cores muito saturadas
- Elementos muito próximos
- Bordas grossas ou sólidas
- Sombras pesadas (drop-shadow)

---

## Responsividade

### Breakpoints

| Dispositivo | Largura |
|-------------|---------|
| Mobile | < 768px |
| Tablet | 768px - 1024px |
| Desktop | > 1024px |

### Adaptações Mobile

- Título hero: reduzir para 36px - 48px
- Menu: hamburguer
- Padding: reduzir para 16px - 20px
- Texto: manter legível (min 14px)

---

## Exemplo de Implementação

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Landing Page</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      min-height: 100vh;
      background: linear-gradient(135deg, #1a1030 0%, #4a2c6a 50%, #8b5a8c 100%);
      color: white;
    }

    .header {
      position: fixed;
      top: 0;
      width: 100%;
      padding: 20px 40px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .hero {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 0 20px;
    }

    .hero h1 {
      font-size: 72px;
      font-weight: 100;
      letter-spacing: 0.3em;
      margin-bottom: 32px;
    }

    .hero p {
      max-width: 600px;
      font-size: 14px;
      line-height: 1.7;
      color: rgba(255, 255, 255, 0.8);
      margin-bottom: 32px;
    }

    .btn-cta {
      background: transparent;
      border: 1px solid rgba(255, 255, 255, 0.5);
      border-radius: 25px;
      padding: 14px 36px;
      color: white;
      font-size: 14px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .btn-cta:hover {
      background: rgba(255, 255, 255, 0.1);
      border-color: white;
    }
  </style>
</head>
<body>
  <header class="header">
    <!-- Navegação aqui -->
  </header>

  <section class="hero">
    <h1>WELCOME</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    <button class="btn-cta">LEARN MORE</button>
  </section>
</body>
</html>
```

---

## Checklist de Implementação

- [ ] Gradiente de fundo configurado
- [ ] Tipografia thin/light para títulos
- [ ] Espaçamentos generosos aplicados
- [ ] Botões com bordas arredondadas
- [ ] Transparências e hover states
- [ ] Responsividade testada
- [ ] Contraste de texto adequado
