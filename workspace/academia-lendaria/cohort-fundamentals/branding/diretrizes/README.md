# Diretrizes de Design - Cohort Essentials

> **Sistema de Design extraído de:** https://cohorts.academialendaria.ai/
> **Data:** 2026-02-02
> **Gerado por:** Design Analyst - Sleep Agent (Extensão Branding & Visual)

---

## 📁 Arquivos Neste Diretório

### 1. `DIRETRIZES-DESIGN.md`
**Documentação completa de design** com:
- Princípios fundamentais
- Sistema de cores completo (primárias, estados, neutras)
- Sistema tipográfico (escalas, pesos, line-heights)
- Sistema de espaçamento (grid 8pt)
- Especificações de componentes
- Efeitos visuais (sombras, glows, gradientes)
- Do's and Don'ts
- Guidelines de acessibilidade
- Estrutura atômica (Atomic Design)

**Público-alvo:** Designers, Product Managers, Desenvolvedores

---

### 2. `design-tokens.json`
**Tokens de design em formato JSON** para integração com ferramentas como:
- Style Dictionary
- Figma Tokens
- Design systems automatizados
- Pipelines de build

**Como usar:**
```javascript
import tokens from './design-tokens.json';

const primaryColor = tokens.colors.primary.gold; // "#C9A227"
const spacing = tokens.spacing['4']; // "1rem"
```

---

### 3. `tokens.css`
**Variáveis CSS prontas para uso** com:
- CSS Custom Properties (`:root`)
- Utility classes para rapid prototyping
- Comentários organizados por categoria

**Como usar:**

**Opção 1 - Importar no CSS:**
```css
@import './tokens.css';

.meu-componente {
  background: var(--color-bg-card);
  padding: var(--space-4);
  border-radius: var(--radius-md);
  color: var(--color-text-primary);
}
```

**Opção 2 - Usar utility classes:**
```html
<div class="bg-card p-4 rounded-md text-primary shadow-card">
  Meu conteúdo
</div>
```

---

## 🎨 Destaques do Sistema

### Paleta de Cores Dark Mode
- **Gold (`#C9A227`)**: Ações principais, conteúdo prioritário
- **Purple (`#A855F7`)**: Conteúdo avançado, maestria
- **Teal (`#134E4A`)**: Módulos de profundidade

### Tipografia
- **Fonte:** Inter (system fallbacks)
- **Escala:** 12px (xs) até 48px (5xl)
- **Sistema:** Modular scale com line-heights otimizados

### Espaçamento
- **Base:** Sistema de 8pt (4px, 8px, 12px, 16px, 24px, 32px...)
- **Consistência:** Todos os espaçamentos seguem a escala

### Componentes
- Cards com estados hover
- Botões (primary, secondary, ghost)
- Badges com variantes coloridas
- Progress steps circulares
- Inputs com estados de foco/erro

---

## 🚀 Próximos Passos

### Para Designers
1. Criar biblioteca de componentes no Figma baseada nas diretrizes
2. Exportar assets seguindo o sistema de cores
3. Documentar padrões de interação e micro-animações

### Para Desenvolvedores
1. Importar `tokens.css` no projeto
2. Criar componentes React/Vue baseados nas especificações
3. Implementar temas usando CSS Custom Properties
4. Configurar Style Dictionary se necessário

### Para Product Managers
1. Revisar princípios fundamentais
2. Validar alinhamento com objetivos do produto
3. Definir roadmap de implementação dos componentes

---

## 📚 Referências Metodológicas

As diretrizes foram criadas com base em:
- **Grid Systems** (Josef Muller-Brockmann)
- **10 Principles of Good Design** (Dieter Rams)
- **Atomic Design** (Brad Frost)
- **Material Design 8pt System** (Google)
- **Dark Mode Best Practices**

---

## 🔄 Atualizações

| Versão | Data | Mudanças |
|--------|------|----------|
| 1.0 | 2026-02-02 | Extração inicial do design system |

---

## 📞 Contato

Para dúvidas ou atualizações neste sistema de design:
- Use o comando `/design-analyst` no Sleep Agent
- Consulte a extensão **Branding & Visual**

---

## 📄 Licença

Este sistema de design é baseado na análise da plataforma **Academia Lendária** e deve ser usado exclusivamente para o produto **Cohort Essentials**.
