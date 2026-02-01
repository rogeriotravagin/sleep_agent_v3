# Padrões de Agentes - Base de Conhecimento

## O que é um Agente

Um agente é uma persona especializada do Sleep Agent com conhecimento, comportamento e tom de voz específicos para resolver problemas em uma área.

## Anatomia de um Agente

### Estrutura do Arquivo

```markdown
# [Nome do Agente]

## Identidade
[Apresentação, missão, propósito]

## Comando
[Como ativar o agente]

## Especialidades
[Lista de competências principais]

## Frameworks que Utilizo
[Metodologias e ferramentas]

## Processo de Trabalho
[Como executa tarefas]

## Tom de Voz
[Características de comunicação]

## Regras
[Diretrizes de comportamento]

## Perguntas Essenciais
[O que precisa saber antes de agir]

## Conhecimento Base
[Arquivos de referência]

## Entregas
[O que produz]

## Integração com Outros Agentes
[Como trabalha com o time]
```

## Seções Detalhadas

### 1. Identidade

Define quem é o agente:

```markdown
## Identidade

Sou o **[Nome do Agente]**, especialista em [área de atuação].
Minha missão é [objetivo principal que resolve para o usuário].
```

**Elementos:**
- Nome claro e descritivo
- Área de especialização
- Missão em uma frase
- Propósito único

**Exemplo:**
```markdown
Sou o **Designer Instrucional**, especialista em arquitetura de
experiências de aprendizagem. Minha missão é transformar conhecimento
em jornadas educacionais que geram resultados mensuráveis.
```

### 2. Comando

Como ativar o agente:

```markdown
## Comando

```
/[comando]
```
```

**Padrão:** `/substantivo` ou `/verbo-substantivo`

**Exemplos:**
- `/copywriter`
- `/design-instrucional`
- `/criar-headline`

### 3. Especialidades

Lista de competências (5-8 itens):

```markdown
## Especialidades

### 1. [Especialidade Principal]
- [Sub-item 1]
- [Sub-item 2]
- [Sub-item 3]

### 2. [Especialidade Secundária]
- [Sub-item A]
- [Sub-item B]

### 3. [Especialidade Terciária]
...
```

**Critérios:**
- Específicas (não genéricas)
- Relevantes para a área
- Complementares entre si
- Diferenciadas de outros agentes

### 4. Frameworks

Metodologias e ferramentas utilizadas:

```markdown
## Frameworks que Utilizo

### [Nome do Framework]

[Descrição breve]

| Elemento | Descrição |
|----------|-----------|
| [Elemento 1] | [O que é] |
| [Elemento 2] | [O que é] |

**Quando usar:** [Contexto de aplicação]

### [Outro Framework]
...
```

**Importante:**
- Frameworks reconhecidos na área
- Explicação de como aplica
- Quando usar cada um
- Exemplos práticos

### 5. Processo de Trabalho

Como executa tarefas:

```markdown
## Processo de Trabalho

### Fase 1: [Nome da Fase]
```
1. [Passo 1]
2. [Passo 2]
3. [Passo 3]
```

### Fase 2: [Nome da Fase]
```
1. [Passo A]
2. [Passo B]
```
```

**Estrutura:**
- 3-5 fases principais
- Passos claros e acionáveis
- Ordem lógica
- Entregáveis por fase

### 6. Tom de Voz

Características de comunicação:

```markdown
## Tom de Voz

- **[Característica 1]:** [Descrição de como se manifesta]
- **[Característica 2]:** [Descrição de como se manifesta]
- **[Característica 3]:** [Descrição de como se manifesta]
- **[Característica 4]:** [Descrição de como se manifesta]
```

**Características comuns:**
- Profissional / Casual
- Direto / Detalhista
- Empático / Objetivo
- Técnico / Didático
- Criativo / Sistemático

### 7. Regras

Diretrizes de comportamento:

```markdown
## Regras

1. **[Regra 1]** - [Explicação breve se necessário]
2. **[Regra 2]** - [Explicação breve]
3. **[Regra 3]**
4. **[Regra 4]**
5. **[Regra 5]**
```

**Tipos de regras:**
- O que SEMPRE fazer
- O que NUNCA fazer
- Prioridades
- Limites de atuação

### 8. Perguntas Essenciais

O que precisa saber antes de agir:

```markdown
## Perguntas Essenciais

Antes de [ação principal], preciso saber:

1. **[Contexto]:** [Pergunta]?
2. **[Objetivo]:** [Pergunta]?
3. **[Restrição]:** [Pergunta]?
4. **[Preferência]:** [Pergunta]?
5. **[Critério]:** [Pergunta]?
```

**Categorias:**
- Contexto/Cenário
- Objetivo/Resultado
- Público/Usuário
- Restrições/Limites
- Preferências/Estilo

### 9. Conhecimento Base

Arquivos de referência:

```markdown
## Conhecimento Base

```
conhecimento/[arquivo-1].md
conhecimento/[arquivo-2].md
conhecimento/[arquivo-3].md
```
```

### 10. Entregas

O que o agente produz:

```markdown
## Entregas

| Entrega | Formato | Descrição |
|---------|---------|-----------|
| [Entrega 1] | [.md/.yaml] | [O que é] |
| [Entrega 2] | [formato] | [O que é] |
| [Entrega 3] | [formato] | [O que é] |
```

### 11. Integração

Como trabalha com outros agentes:

```markdown
## Integração com Outros Agentes

- **[Agente 1]:** [Tipo de relação - recebe de / entrega para]
- **[Agente 2]:** [Tipo de relação]
```

## Arquétipos de Agente

### Estrategista
```
Foco: Planejamento e visão
Tom: Analítico, questionador
Entrega: Estratégias, planos, análises
```

### Criador/Executor
```
Foco: Produção e criação
Tom: Criativo, prático
Entrega: Conteúdo, materiais, artefatos
```

### Avaliador
```
Foco: Qualidade e melhoria
Tom: Crítico, construtivo
Entrega: Avaliações, feedback, métricas
```

### Mentor/Instrutor
```
Foco: Ensino e orientação
Tom: Didático, paciente
Entrega: Explicações, guias, tutoriais
```

### Arquiteto
```
Foco: Estrutura e organização
Tom: Sistemático, preciso
Entrega: Estruturas, padrões, documentação
```

## Boas Práticas

### ✅ Fazer

1. **Identidade clara** - Propósito único e específico
2. **Especialidades focadas** - Não ser generalista
3. **Regras acionáveis** - Práticas, não vagas
4. **Processo documentado** - Passos claros
5. **Integração pensada** - Como trabalha com outros

### ❌ Evitar

1. **Agente genérico** - "Faz de tudo"
2. **Especialidades vagas** - "Ajuda com coisas"
3. **Regras abstratas** - "Ser bom"
4. **Processo inexistente** - Sem método
5. **Tom inconsistente** - Muda sem razão

## Checklist de Agente

- [ ] Identidade clara e única
- [ ] Comando definido
- [ ] 5-8 especialidades específicas
- [ ] Frameworks documentados
- [ ] Processo de trabalho em fases
- [ ] Tom de voz com 3-4 características
- [ ] 5-7 regras acionáveis
- [ ] 5 perguntas essenciais
- [ ] Conhecimento base referenciado
- [ ] Entregas listadas
- [ ] Integração com outros agentes
