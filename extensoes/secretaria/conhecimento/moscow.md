# MoSCoW Method

Técnica de priorização usada em gestão de projetos e produtos para classificar requisitos e features.

## Origem

Criado por Dai Clegg na década de 1990 para desenvolvimento ágil de software. Nome é acrônimo de Must, Should, Could, Won't.

## As 4 Categorias

### M - Must Have (Obrigatório)

**Definição:** Requisitos críticos sem os quais o projeto/produto FALHA.

**Características:**
- Não negociável
- Sistema quebra ou não funciona sem isso
- Legal/regulatório obrigatório
- Bloqueia tudo se não for feito

**Perguntas:**
- O que acontece se não for feito? (Resposta: Projeto falha)
- Isso é legal/contratualment obrigatório?
- O produto funciona sem isso? (Resposta: Não)

**Exemplos:**
- Sistema de pagamento em e-commerce (sem isso, não vende)
- Login em plataforma (sem isso, não acessa)
- Conformidade legal (sem isso, multa/processo)

### S - Should Have (Importante)

**Definição:** Importante mas não crítico. Sistema funciona sem, mas limitado.

**Características:**
- Alta prioridade mas não mata o projeto
- Pode ser adiado se necessário
- Entrega com valor reduzido sem isso
- Geralmente vai na primeira release

**Perguntas:**
- O produto funciona sem isso? (Resposta: Funciona mas limitado)
- Usuários ficariam frustrados sem isso? (Resposta: Sim, mas usariam mesmo assim)

**Exemplos:**
- Filtros avançados em busca (busca básica funciona)
- Notificações por email (app funciona sem)
- Dashboard de analytics (sistema funciona, mas falta visibilidade)

### C - Could Have (Desejável)

**Definição:** Nice to have. Melhora experiência mas não essencial.

**Características:**
- Baixa prioridade
- Facilmente removível se necessário
- "Seria legal ter"
- Pode ir em releases futuras

**Perguntas:**
- Isso melhora a experiência? (Resposta: Sim, mas pouco)
- Faria diferença significativa? (Resposta: Não muita)

**Exemplos:**
- Tema escuro
- Atalhos de teclado extras
- Animações polidas
- Features "de luxo"

### W - Won't Have (Não Terá)

**Definição:** Explicitamente FORA do escopo deste projeto/sprint.

**Características:**
- Menos importante de todas
- Pode ser futuro ou nunca
- Importante documentar para evitar scope creep

**Perguntas:**
- Isso é realmente necessário? (Resposta: Não agora)
- Vale o esforço? (Resposta: Não neste momento)

**Exemplos:**
- Integração com ferramenta X (não é prioridade)
- Feature complexa para < 1% dos usuários
- Otimizações prematuras

**⚠️ Importante:** Won't não significa "nunca". Significa "não AGORA".

---

## Como Usar MoSCoW

### Passo 1: Listar Requisitos/Features

Liste tudo que poderia ser feito.

### Passo 2: Classificar

Para cada item:

1. **É obrigatório para funcionar?**
   - Sim → Must Have
   - Não → próxima pergunta

2. **É importante para experiência/valor?**
   - Sim, muito → Should Have
   - Sim, um pouco → Could Have
   - Não → Won't Have

3. **Validar com stakeholders**

### Passo 3: Priorizar Dentro de Cada Categoria

Dentro de Must, Should, Could - numerar por prioridade:
- M1, M2, M3...
- S1, S2, S3...
- C1, C2, C3...

### Passo 4: Executar em Ordem

1. Todos os Must Haves primeiro
2. Should Haves (tempo permitindo)
3. Could Haves (se sobrar tempo)
4. Won't Haves ficam para depois

---

## Regras de Distribuição

**Recomendação padrão:**
- **Must:** 60% dos requisitos
- **Should:** 20% dos requisitos
- **Could:** 20% dos requisitos
- **Won't:** Quantos forem necessários

**⚠️ Alerta:** Se > 80% são "Must", provavelmente está classificando errado.

**Teste:** Pergunte "Se tivéssemos que entregar em 50% do tempo, o que cortaríamos?"
- Resposta mostra os reais Must vs Should.

---

## MoSCoW vs Outras Metodologias

### vs Eisenhower

| Eisenhower | MoSCoW Equivalente |
|------------|-------------------|
| Q1 (Urgente + Importante) | Must Have |
| Q2 (Importante + Não Urgente) | Should Have |
| Q3 (Urgente + Não Importante) | Could Have |
| Q4 (Desperdício) | Won't Have |

### vs Sistema ABC

| ABC | MoSCoW Equivalente |
|-----|-------------------|
| A (Crítico) | Must Have |
| B (Importante) | Should Have |
| C (Desejável) | Could Have + Won't |

---

## Aplicações Práticas

### Para Product Management

Priorizar backlog:
```
Sprint 1:
- [M1] Login system
- [M2] Payment integration
- [S1] Email notifications
- [C1] Dark mode (se sobrar tempo)

Sprint 2:
- [S2] Advanced filters
- [S3] Analytics dashboard
- [C2] Keyboard shortcuts

Futuro (Won't):
- [W] Integration with tool X
- [W] Mobile app
```

### Para Projetos

Definir escopo de MVP:
```
MVP (Minimum Viable Product):
✅ Must Haves (apenas estes)

V1.1:
✅ Should Haves

V2.0:
✅ Could Haves

Backlog:
📋 Won't Haves (reavaliar depois)
```

### Para Decisões Pessoais

Priorizar tarefas:
```
Hoje (Must):
- Entregar proposta cliente
- Reunião com equipe

Esta semana (Should):
- Preparar apresentação
- Review de código

Quando possível (Could):
- Organizar arquivos
- Ler artigo técnico

Não agora (Won't):
- Aprender framework novo
- Refatorar código antigo
```

---

## Armadilhas Comuns

### 1. Tudo é "Must Have"

**Sintoma:** 90% classificado como Must.
**Problema:** Perde o poder de priorização.
**Solução:** Perguntar "O que acontece se não for feito?" Ser honesto sobre "falha" vs "limitação".

### 2. "Should" virando "Must" por pressão

**Sintoma:** Stakeholder insistindo que "Should é Must na verdade".
**Problema:** Scope creep.
**Solução:** Usar definição objetiva: "Sistema quebra sem isso?" Se não, não é Must.

### 3. Não documentar "Won't"

**Problema:** Expectativas não alinhadas, discussões repetidas.
**Solução:** Documentar explicitamente o que NÃO será feito e por quê.

### 4. Ignorar capacidade realista

**Problema:** 20 Must Haves para 1 sprint.
**Solução:** Must Have deve caber no tempo disponível. Se não cabe, reavaliar o que é REALMENTE must.

---

## Template de Uso

```markdown
# Priorização MoSCoW: [Projeto/Sprint]

## Must Have (Obrigatório) 🔴
- [ ] M1: [Item] - [Por quê é Must]
- [ ] M2: [Item] - [Por quê é Must]
- [ ] M3: [Item] - [Por quê é Must]

**Validação:** Sistema funciona sem estes? NÃO.

## Should Have (Importante) 🟡
- [ ] S1: [Item] - [Por quê é Should]
- [ ] S2: [Item] - [Por quê é Should]

**Validação:** Sistema funciona sem estes? SIM, mas limitado.

## Could Have (Desejável) 🟢
- [ ] C1: [Item] - [Por quê é Could]
- [ ] C2: [Item] - [Por quê é Could]

**Validação:** Nice to have, não essencial.

## Won't Have (Fora do Escopo) ⚪
- W1: [Item] - [Por quê não agora]
- W2: [Item] - [Por quê não agora]

**Revisão futura:** [Data de reavaliação]

---

**Decisão Final:** [Data] | **Aprovado por:** [Stakeholder]
```

---

## Referências

- [MoSCoW Method - Wikipedia](https://en.wikipedia.org/wiki/MoSCoW_method)
- Clegg, Dai & Barker, Richard. "Case Method Fast-Track: A RAD Approach" (1994)
- [MoSCoW Prioritization](https://www.productplan.com/glossary/moscow-prioritization/)
