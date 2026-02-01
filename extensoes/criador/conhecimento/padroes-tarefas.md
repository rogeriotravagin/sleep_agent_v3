# Padrões de Tarefas - Base de Conhecimento

## O que é uma Tarefa

Uma tarefa é uma ação específica que um agente executa, com entradas definidas, processo estruturado e saída padronizada.

## Estrutura de Arquivo .yaml

```yaml
# ============================================
# TAREFA: [Nome Descritivo]
# ============================================

# Identificação
id: nome-da-tarefa
nome: Nome Descritivo da Tarefa
descricao: Descrição do que a tarefa entrega
agente: id-do-agente
comando: /comando
versao: "1.0"
categoria: criacao|analise|estrategia|automacao

# Entradas
entradas:
  obrigatorias:
    - nome: entrada_1
      pergunta: "Pergunta para o usuário?"
      tipo: texto|lista|escolha|numero
      exemplo: "Exemplo de resposta"

    - nome: entrada_2
      pergunta: "Outra pergunta?"
      tipo: escolha
      opcoes:
        - "Opção 1"
        - "Opção 2"
        - "Opção 3"
      padrao: "Opção 1"

  opcionais:
    - nome: entrada_opcional
      pergunta: "Pergunta opcional?"
      tipo: texto
      padrao: "Valor padrão"

# Processo
passos:
  - numero: 1
    acao: "Descrição do que fazer"
    detalhes:
      - "Detalhe 1"
      - "Detalhe 2"

  - numero: 2
    acao: "Próximo passo"

# Saída
saida:
  formato: markdown|yaml|json|texto
  local: output/[tipo]/
  template: |
    # Título

    ## Seção 1
    {{variavel_1}}

    ## Seção 2
    {{variavel_2}}

# Conhecimento
conhecimento:
  - arquivo-1.md
  - arquivo-2.md

# Validação
gates:
  - "Pergunta de validação 1?"
  - "Pergunta de validação 2?"

# Continuação
proximos_passos:
  - "Sugestão de próxima tarefa"
  - "Outra sugestão"
```

## Campos Detalhados

### Identificação

```yaml
id: criar-headline
nome: Criar Headlines que Convertem
descricao: Gera múltiplas headlines usando fórmulas comprovadas
agente: copywriter
comando: /criar-headline
versao: "1.0"
categoria: criacao
```

| Campo | Descrição | Obrigatório |
|-------|-----------|-------------|
| id | Identificador único (kebab-case) | ✅ |
| nome | Nome descritivo | ✅ |
| descricao | O que entrega | ✅ |
| agente | ID do agente responsável | ✅ |
| comando | Comando para executar | ✅ |
| versao | Versão semântica | ✅ |
| categoria | Tipo da tarefa | ✅ |

**Categorias disponíveis:**
- `criacao` - Criar algo novo
- `analise` - Analisar algo existente
- `estrategia` - Definir estratégia
- `automacao` - Processos automáticos
- `planejamento` - Planejar ações
- `avaliacao` - Avaliar qualidade

### Entradas

#### Obrigatórias

```yaml
entradas:
  obrigatorias:
    - nome: produto
      pergunta: "O que você está vendendo?"
      tipo: texto
      exemplo: "Curso de confeitaria online"

    - nome: nivel
      pergunta: "Qual o nível?"
      tipo: escolha
      opcoes:
        - "Iniciante"
        - "Intermediário"
        - "Avançado"
      padrao: "Iniciante"
```

#### Opcionais

```yaml
  opcionais:
    - nome: quantidade
      pergunta: "Quantas criar?"
      tipo: numero
      padrao: 5

    - nome: estilo
      pergunta: "Algum estilo específico?"
      tipo: texto
```

**Tipos de entrada:**

| Tipo | Descrição | Exemplo |
|------|-----------|---------|
| texto | Campo livre | "Descreva seu produto" |
| lista | Múltiplos itens | ["Item 1", "Item 2"] |
| escolha | Uma opção | "Opção A" ou "Opção B" |
| numero | Valor numérico | 5, 10, 100 |

### Passos

```yaml
passos:
  - numero: 1
    acao: "Coletar informações essenciais"
    detalhes:
      - "Verificar dados obrigatórios"
      - "Validar formato das entradas"
      - "Identificar lacunas"

  - numero: 2
    acao: "Analisar contexto"
    detalhes:
      - "Entender o público-alvo"
      - "Mapear concorrência"

  - numero: 3
    acao: "Executar tarefa principal"

  - numero: 4
    acao: "Validar resultado"
    detalhes:
      - "Verificar gates de qualidade"
      - "Ajustar se necessário"

  - numero: 5
    acao: "Entregar e sugerir próximos passos"
```

**Boas práticas:**
- 4-7 passos por tarefa
- Verbos de ação no infinitivo
- Detalhes quando necessário
- Ordem lógica

### Saída

```yaml
saida:
  formato: markdown
  local: output/headlines/
  template: |
    # Headlines Criadas

    ## Contexto
    - **Produto:** {{produto}}
    - **Público:** {{publico}}
    - **Benefício:** {{beneficio}}

    ## Headlines

    **1. [Categoria: Benefício Direto]**
    > {{headline_1}}
    Por que funciona: {{razao_1}}

    **2. [Categoria: Curiosidade]**
    > {{headline_2}}
    Por que funciona: {{razao_2}}

    ## Minha Recomendação
    A headline **#{{favorita}}** é a mais forte porque {{razao_favorita}}.

    ## Próximos Passos
    - [ ] Testar em anúncio
    - [ ] Criar variações para A/B test
```

**Formatos:**
- `markdown` - Documentos estruturados
- `yaml` - Configurações
- `json` - Dados estruturados
- `texto` - Texto simples

### Conhecimento

```yaml
conhecimento:
  - conhecimento/copywriting.md
  - conhecimento/formulas.md
  - conhecimento/gatilhos.md
```

Lista de arquivos de referência que o agente deve consultar.

### Gates de Qualidade

```yaml
gates:
  - "Cada headline tem uma ideia clara?"
  - "Evitou clichês e termos genéricos?"
  - "Benefício está explícito?"
  - "Tamanho adequado (5-15 palavras)?"
  - "Responde às necessidades do público?"
```

Perguntas de verificação antes de entregar o resultado.

### Próximos Passos

```yaml
proximos_passos:
  - "Criar variações para teste A/B"
  - "Desenvolver subheadline"
  - "Criar lead/abertura baseada"
```

Sugestões de continuação do trabalho.

## Exemplos por Categoria

### Tarefa de Criação

```yaml
id: criar-email
nome: Criar Email de Vendas
descricao: Criar email persuasivo para campanha de vendas
agente: copywriter
comando: /criar-email
categoria: criacao

entradas:
  obrigatorias:
    - nome: objetivo
      pergunta: "Qual o objetivo do email?"
      tipo: escolha
      opcoes: ["Venda direta", "Nutrição", "Lançamento"]

    - nome: produto
      pergunta: "O que está vendendo?"
      tipo: texto
```

### Tarefa de Análise

```yaml
id: analisar-concorrencia
nome: Analisar Concorrência
descricao: Mapear e analisar principais concorrentes
agente: estrategista
comando: /analisar-concorrencia
categoria: analise

entradas:
  obrigatorias:
    - nome: concorrentes
      pergunta: "Quais concorrentes analisar?"
      tipo: lista
      exemplo: ["Concorrente A", "Concorrente B"]
```

### Tarefa de Estratégia

```yaml
id: criar-posicionamento
nome: Definir Posicionamento
descricao: Criar posicionamento único de marca
agente: estrategista
comando: /posicionamento
categoria: estrategia

entradas:
  obrigatorias:
    - nome: mercado
      pergunta: "Qual seu mercado?"
      tipo: texto

    - nome: diferenciais
      pergunta: "Quais seus diferenciais?"
      tipo: lista
```

## Checklist de Tarefa

### Identificação ✓
- [ ] ID único em kebab-case
- [ ] Nome descritivo
- [ ] Descrição clara do resultado
- [ ] Agente vinculado
- [ ] Comando definido
- [ ] Categoria correta

### Entradas ✓
- [ ] Entradas obrigatórias definidas
- [ ] Perguntas claras
- [ ] Tipos corretos
- [ ] Exemplos fornecidos
- [ ] Opcionais com valores padrão

### Processo ✓
- [ ] 4-7 passos
- [ ] Ordem lógica
- [ ] Verbos de ação
- [ ] Detalhes quando necessário

### Saída ✓
- [ ] Formato definido
- [ ] Local de salvamento
- [ ] Template completo
- [ ] Variáveis mapeadas

### Qualidade ✓
- [ ] Conhecimento referenciado
- [ ] Gates de qualidade
- [ ] Próximos passos sugeridos
