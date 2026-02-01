# Extensão Criador - Sleep Agent

Meta-framework interno para criar novas extensões, agentes, tarefas e workflows de forma padronizada.

## Visão Geral

A extensão **Criador** é o motor interno do Sleep Agent para expandir o sistema. Ela documenta e automatiza o processo de criação de novas áreas especializadas.

### Para que serve

- Criar novas extensões (como Marketing, Branding, Educacional)
- Padronizar a estrutura de agentes e workflows
- Automatizar criação via Ralph
- Garantir consistência em todo o sistema

## Comandos Rápidos

```bash
# Criar extensão rapidamente (5 perguntas)
/iniciante-extensao

# Workflow completo de extensão
/extensao-completa

# Tarefas específicas
/criar-extensao        # Estrutura de extensão
/criar-agente          # Novo agente
/criar-tarefa          # Nova tarefa
/criar-workflow-extensao  # Novo workflow
/criar-conhecimento    # Base de conhecimento
```

## Agentes Especializados

| Agente | Comando | Especialidade |
|--------|---------|---------------|
| Arquiteto de Extensões | `/arquiteto` | Estrutura e arquitetura |
| Designer de Agentes | `/designer-agente` | Criação de agentes |
| Criador de Workflows | `/criar-workflow` | Design de workflows |

## Estrutura Padrão de Extensão

Toda extensão do Sleep Agent segue esta estrutura:

```
extensoes/[nome]/
├── extensao.yaml              # Configuração principal
├── README.md                  # Documentação
├── agentes/                   # Agentes especializados
│   ├── AGENTE-1.md
│   ├── AGENTE-2.md
│   └── ...
├── conhecimento/              # Base de conhecimento
│   ├── tema-1.md
│   ├── tema-2.md
│   └── ...
├── tarefas/                   # Tarefas disponíveis
│   ├── tarefa-1.yaml
│   ├── tarefa-2.yaml
│   └── ...
├── workflows/                 # Workflows completos
│   ├── workflow-1.yaml
│   └── ...
└── exemplos/                  # Exemplos de saída
    └── ...
```

## Processo de Criação

### Modo Iniciante (`/iniciante-extensao`)

1. **5 Perguntas:**
   - Qual área/tema?
   - Quem vai usar?
   - Quais os principais problemas?
   - Quais resultados esperados?
   - Quantos agentes?

2. **Processamento:**
   - Sistema define estrutura
   - Cria agentes base
   - Gera tarefas principais
   - Prepara PRD para Ralph

3. **Ralph:**
   - Gera extensão completa
   - Cria documentação
   - Configura integrações

### Modo Completo (`/extensao-completa`)

7 fases profissionais:

1. **DESCOBERTA** - Entender escopo e necessidades
2. **ARQUITETURA** - Definir estrutura e componentes
3. **AGENTES** - Criar agentes especializados
4. **CONHECIMENTO** - Desenvolver base de conhecimento
5. **TAREFAS** - Criar tarefas disponíveis
6. **WORKFLOWS** - Criar workflows completos
7. **INTEGRAÇÃO** - Registrar no sistema e testar

## Padrões Obrigatórios

### Nomenclatura

| Elemento | Padrão | Exemplo |
|----------|--------|---------|
| Extensão | kebab-case | `educacional`, `financeiro` |
| Agente | MAIÚSCULA.md | `COPYWRITER.md` |
| Tarefa | kebab-case.yaml | `criar-headline.yaml` |
| Workflow | kebab-case.yaml | `curso-completo.yaml` |
| Comando | /slug | `/marketing`, `/criar-aula` |

### Arquivo extensao.yaml

Campos obrigatórios:
- `nome`, `slug`, `versao`
- `comando`, `status`
- `descricao`
- `agentes[]`
- `tarefas[]`
- `conhecimento[]`

### Arquivo de Agente (.md)

Seções obrigatórias:
- Identidade
- Comando
- Especialidades
- Frameworks/Metodologias
- Processo de Trabalho
- Tom de Voz
- Regras
- Conhecimento Base

### Arquivo de Tarefa (.yaml)

Campos obrigatórios:
- `id`, `nome`, `descricao`
- `agente`, `comando`
- `entradas` (obrigatórias e opcionais)
- `passos`
- `saida` com template
- `gates` de qualidade

### Arquivo de Workflow (.yaml)

Campos obrigatórios:
- `id`, `nome`, `descricao`
- `comando`, `versao`
- `fases[]` com etapas
- `entrega_final`
- `execucao`

## Integração com Ralph

A extensão inclui templates para geração via Ralph:

```bash
# Gerar extensão automaticamente
./frameworks/ralph/scripts/ralph.sh 30

# Templates disponíveis
frameworks/ralph/templates/prd-extensao.json
frameworks/ralph/templates/prompt-extensao.md
```

## Checklist de Nova Extensão

### Estrutura
- [ ] Diretório criado em `extensoes/`
- [ ] `extensao.yaml` configurado
- [ ] `README.md` documentado
- [ ] Diretórios internos criados

### Agentes
- [ ] Pelo menos 1 agente criado
- [ ] Identidade definida
- [ ] Especialidades listadas
- [ ] Regras documentadas

### Tarefas
- [ ] Tarefas principais criadas
- [ ] Entradas bem definidas
- [ ] Templates de saída
- [ ] Gates de qualidade

### Workflows
- [ ] Pelo menos 1 workflow
- [ ] Fases documentadas
- [ ] Checkpoints definidos
- [ ] Integração com Ralph (se aplicável)

### Conhecimento
- [ ] Base de conhecimento criada
- [ ] Referências listadas
- [ ] Metodologias documentadas

### Integração
- [ ] `delegacao.yaml` atualizado
- [ ] `CLAUDE.md` atualizado
- [ ] Pastas de output criadas
- [ ] Testes realizados

## Extensões Criadas

| Extensão | Data | Agentes | Tarefas |
|----------|------|---------|---------|
| Marketing | v1.0 | 3 | 8 |
| Branding | v1.0 | 3 | 7 |
| Educacional | v1.0 | 3 | 7 |

## Uso Avançado

### Criar Extensão para Área Específica

```
/extensao-completa

Área: Financeiro
Público: Gestores financeiros
Problemas: Orçamento, fluxo de caixa, investimentos
Resultados: Relatórios, análises, projeções
```

### Adicionar Agente a Extensão Existente

```
/criar-agente

Extensão: marketing
Nome: Analista de Dados
Especialidades: Analytics, métricas, dashboards
```

### Criar Workflow Personalizado

```
/criar-workflow-extensao

Extensão: educacional
Nome: Revisão de Curso
Fases: Análise, Feedback, Ajustes, Validação
```
