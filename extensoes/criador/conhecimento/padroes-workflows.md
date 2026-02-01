# Padrões de Workflows - Base de Conhecimento

## O que é um Workflow

Um workflow é um processo estruturado com múltiplas fases que guia o usuário do início ao resultado final, orquestrando agentes e tarefas.

## Tipos de Workflow

### 1. Modo Iniciante
```
Características:
- Máximo 5 perguntas
- Processamento automático
- Integração com Ralph
- Resultado rápido (10-15 min)

Estrutura:
BRIEFING → PROCESSAMENTO → RALPH → ENTREGA
```

### 2. Modo Completo
```
Características:
- Múltiplas fases detalhadas
- Interação em cada etapa
- Checkpoints de validação
- Resultado profissional (horas/dias)

Estrutura:
DESCOBERTA → [FASES ESPECÍFICAS] → ENTREGA
```

### 3. Workflow Rápido
```
Características:
- Foco único
- Poucas fases (2-3)
- Execução rápida
- Resultado específico

Estrutura:
ENTRADA → EXECUÇÃO → SAÍDA
```

## Estrutura de Arquivo .yaml

```yaml
# ============================================
# WORKFLOW: [Nome do Workflow]
# ============================================

id: nome-do-workflow
nome: Nome Descritivo do Workflow
descricao: Descrição do que o workflow entrega
comando: /comando
versao: "1.0"

# Visão Geral
visao_geral:
  objetivo: "Descrição do objetivo final"
  duracao_estimada: "X minutos/horas"
  resultado: "O que será entregue"
  baseado_em:
    - "Metodologia 1"
    - "Metodologia 2"

# Fases
fases:
  - numero: 1
    nome: FASE_1
    descricao: "O que acontece nesta fase"
    agente: agente-responsavel
    tempo_estimado: "X minutos"

    etapas:
      - id: etapa-1
        nome: "Nome da Etapa"
        descricao: "O que faz"

        perguntas:
          - pergunta: "Pergunta para o usuário?"
            tipo: texto|lista|escolha
            obrigatorio: true
            var: nome_variavel

        processo:
          - "Passo 1"
          - "Passo 2"

        entregavel: arquivo.md
        template_entregavel: |
          # Template
          {{conteudo}}

    checkpoint:
      pergunta: "Validação para prosseguir?"
      acao_se_nao: "O que fazer se não passar"

    saida_fase: |
      ## Fase Concluída
      - Item 1 completo
      - Item 2 completo

  - numero: 2
    nome: FASE_2
    ...

# Entrega Final
entrega_final:
  formato: pasta|arquivo
  local: projetos/[nome]/
  estrutura: |
    [nome]/
    ├── arquivo1.md
    ├── arquivo2.md
    └── pasta/
        └── arquivo3.md

# Execução
execucao:
  comando: /comando
  fluxo:
    1: "Descrição do passo 1"
    2: "Descrição do passo 2"
    3: "Descrição do passo 3"

  mensagem_inicial: |
    ## Início do Workflow
    Mensagem de boas-vindas

  mensagem_final: |
    ## Conclusão
    Mensagem de encerramento

# Fallbacks
fallbacks:
  se_informacao_incompleta:
    acao: perguntar
    mensagem: "Preciso de mais informações sobre X"

  se_erro:
    acao: retry|skip|abort
    mensagem: "Mensagem de erro"
```

## Seções Detalhadas

### Visão Geral

```yaml
visao_geral:
  objetivo: "Criar curso profissional completo"
  duracao_estimada: "3-5 sessões de trabalho"
  resultado: "Curso pronto para lançamento"

  baseado_em:
    - "ADDIE Model"
    - "Backward Design"
    - "Gamification"

  diferencial: |
    Este workflow diferencia-se por...
```

### Fases

#### Estrutura de Fase

```yaml
fases:
  - numero: 1
    nome: DESCOBERTA
    descricao: "Entender contexto, público e objetivos"
    agente: estrategista
    tempo_estimado: "30 minutos"

    etapas:
      - id: briefing
        nome: "Briefing Inicial"
        descricao: "Coletar informações essenciais"

        perguntas:
          - pergunta: "Qual o tema?"
            tipo: texto
            obrigatorio: true
            var: tema

          - pergunta: "Para quem é?"
            tipo: texto
            obrigatorio: true
            var: publico

        entregavel: briefing.md

      - id: analise
        nome: "Análise de Contexto"
        descricao: "Analisar mercado e público"

        processo:
          - "Analisar dados coletados"
          - "Identificar oportunidades"
          - "Mapear desafios"

        entregavel: analise.md

    checkpoint:
      pergunta: "As informações estão claras para prosseguir?"
      acao_se_nao: "Refinar briefing"
```

#### Tipos de Etapa

**Etapa de Coleta:**
```yaml
- id: coleta
  nome: "Coleta de Dados"
  perguntas:
    - pergunta: "Pergunta?"
      tipo: texto
  entregavel: dados.md
```

**Etapa de Processamento:**
```yaml
- id: processamento
  nome: "Processamento"
  automatico: true
  processo:
    - "Ação automática 1"
    - "Ação automática 2"
  entregavel: resultado.md
```

**Etapa de Criação:**
```yaml
- id: criacao
  nome: "Criação"
  usar_tarefa: criar-headline
  repetir_para: "cada item"
  entregavel: headlines/
```

### Entrega Final

```yaml
entrega_final:
  formato: pasta
  local: projetos/curso-{{slug}}/
  estrutura: |
    curso-{{slug}}/
    ├── 01-planejamento/
    │   ├── briefing.md
    │   └── objetivos.md
    ├── 02-estrutura/
    │   └── grade-curricular.md
    ├── 03-conteudo/
    │   └── aulas/
    └── 04-avaliacoes/
        └── exercicios/
```

### Execução

```yaml
execucao:
  comando: /curso-completo

  fluxo:
    1: "Coletar briefing inicial"
    2: "Analisar público-alvo"
    3: "Definir objetivos"
    4: "Criar estrutura"
    5: "Desenvolver conteúdo"
    6: "Criar avaliações"
    7: "Finalizar e entregar"

  mensagem_inicial: |
    ## Criação de Curso

    Vamos criar seu curso em 7 fases.
    Tempo estimado: 3-5 horas de trabalho.

    Vamos começar?

  mensagem_final: |
    ## Curso Criado!

    Seu curso está pronto com:
    - X módulos
    - Y aulas
    - Z exercícios

    Próximos passos sugeridos...
```

### Fallbacks

```yaml
fallbacks:
  se_informacao_incompleta:
    acao: perguntar
    mensagem: "Preciso de mais detalhes sobre {{campo}}."

  se_fase_falhar:
    acao: retry
    tentativas: 3
    mensagem: "Vou tentar novamente..."

  se_usuario_cancelar:
    acao: salvar_progresso
    mensagem: "Progresso salvo. Pode continuar depois com /continuar"
```

## Workflow Modo Iniciante

### Template Completo

```yaml
id: modo-iniciante-[nome]
nome: Modo Iniciante - [Área]
descricao: Criar [resultado] rapidamente com 5 perguntas + Ralph
comando: /iniciante-[nome]
versao: "1.0"

visao_geral:
  objetivo: "Criar [resultado] rapidamente"
  duracao_estimada: "10-15 minutos"
  resultado: "[O que será entregue]"
  integracao_ralph: true

fases:
  - numero: 1
    nome: BRIEFING EXPRESS
    tempo_estimado: "3-5 minutos"

    etapas:
      - id: 5-perguntas
        nome: "5 Perguntas Essenciais"
        perguntas:
          - pergunta: "Pergunta 1?"
            tipo: texto
            var: var1
          - pergunta: "Pergunta 2?"
            tipo: texto
            var: var2
          - pergunta: "Pergunta 3?"
            tipo: texto
            var: var3
          - pergunta: "Pergunta 4?"
            tipo: escolha
            opcoes: [...]
            var: var4
          - pergunta: "Pergunta 5?"
            tipo: texto
            var: var5

  - numero: 2
    nome: PROCESSAMENTO
    automatico: true
    tempo_estimado: "1-2 minutos"

    etapas:
      - id: processar
        automatico: true
        processo:
          - "Analisar entradas"
          - "Expandir informações"
          - "Preparar estrutura"

  - numero: 3
    nome: PREPARAR RALPH
    automatico: true

    etapas:
      - id: prd
        nome: "Montar PRD"
        automatico: true
        entregavel: prd.json

  - numero: 4
    nome: EXECUTAR RALPH

    execucao:
      comando: "./frameworks/ralph/scripts/ralph.sh 30"
      parametros:
        prd: "{{prd_path}}"
        output: "{{output_path}}"

  - numero: 5
    nome: ENTREGA

    etapas:
      - id: apresentar
        nome: "Apresentar Resultado"
        ofertar_refinamentos: true

ralph:
  template_prd: frameworks/ralph/templates/prd-[nome].json
  template_prompt: frameworks/ralph/templates/prompt-[nome].md
```

## Checklist de Workflow

### Estrutura ✓
- [ ] ID único
- [ ] Nome descritivo
- [ ] Comando definido
- [ ] Visão geral completa

### Fases ✓
- [ ] Mínimo 3 fases
- [ ] Cada fase tem agente
- [ ] Etapas com entregáveis
- [ ] Checkpoints definidos

### Execução ✓
- [ ] Fluxo documentado
- [ ] Mensagens inicial e final
- [ ] Fallbacks configurados

### Entrega ✓
- [ ] Formato especificado
- [ ] Estrutura de saída clara
- [ ] Local definido

### Ralph (se aplicável) ✓
- [ ] PRD template criado
- [ ] Prompt template criado
- [ ] Integração configurada
