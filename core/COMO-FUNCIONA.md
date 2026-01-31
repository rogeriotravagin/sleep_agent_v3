# Como o Sleep Agent Funciona

## Visão Geral

O Sleep Agent é um framework que usa o Claude Code como motor para coordenar agentes especializados. Não há código para rodar - tudo funciona através de arquivos de configuração que o Claude lê e segue.

## Conceitos Principais

### 1. Extensões

Extensões são módulos que adicionam capacidades ao Sleep Agent. Cada extensão contém:

- **Agentes**: Personas especializadas (ex: Copywriter, Estrategista)
- **Tarefas**: Fluxos predefinidos para resultados específicos
- **Workflows**: Sequências de tarefas para projetos maiores
- **Conhecimento**: Base de conhecimento que fundamenta as respostas

### 2. Agentes

Agentes são personas que o Claude assume para executar tarefas específicas. Cada agente tem:

- Nome e especialidade
- Tom de voz próprio
- Conhecimentos específicos
- Formato de entrega

### 3. Tarefas

Tarefas são fluxos estruturados que guiam o agente. Incluem:

- Perguntas a fazer ao usuário
- Passos a seguir
- Formato esperado de saída

### 4. Workflows

Workflows são sequências de tarefas que produzem um resultado maior. Por exemplo, um "lançamento" pode incluir:

1. Definir oferta
2. Criar headlines
3. Escrever emails
4. Configurar campanha

## Fluxo de Uso

```
┌─────────────────┐
│   Você digita   │
│   um comando    │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Orquestrador   │
│   identifica    │
│    intenção     │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│    Delega ao    │
│     agente      │
│  especializado  │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Agente executa │
│  usando base de │
│  conhecimento   │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│    Entrega o    │
│    resultado    │
└─────────────────┘
```

## Salvando Resultados

Todos os resultados podem ser salvos na pasta `projetos/`. Use `/salvar` ou aceite quando o agente oferecer.

## Personalizando

Você pode:
- Editar arquivos de conhecimento para adicionar suas preferências
- Criar novas tarefas copiando templates existentes
- Adicionar exemplos próprios na pasta `exemplos/`
