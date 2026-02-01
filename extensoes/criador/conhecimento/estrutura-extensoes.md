# Estrutura de Extensões - Base de Conhecimento

## O que é uma Extensão

Uma extensão é um módulo especializado do Sleep Agent que adiciona capacidades em uma área específica (ex: Marketing, Educacional, Financeiro).

## Arquitetura de Extensão

### Estrutura de Diretórios

```
extensoes/[nome]/
├── extensao.yaml              # Configuração principal
├── README.md                  # Documentação
├── agentes/                   # Agentes especializados
│   ├── AGENTE-1.md
│   ├── AGENTE-2.md
│   └── AGENTE-3.md
├── conhecimento/              # Base de conhecimento
│   ├── tema-1.md
│   ├── tema-2.md
│   └── tema-3.md
├── tarefas/                   # Tarefas disponíveis
│   ├── tarefa-1.yaml
│   ├── tarefa-2.yaml
│   └── tarefa-3.yaml
├── workflows/                 # Workflows completos
│   ├── workflow-principal.yaml
│   ├── modo-iniciante.yaml
│   └── workflow-rapido.yaml
└── exemplos/                  # Exemplos de saída
    ├── exemplo-1.md
    └── exemplo-2.md
```

## Arquivo extensao.yaml

### Estrutura Completa

```yaml
# ============================================
# EXTENSÃO [NOME] - Sleep Agent
# ============================================

# Metadados obrigatórios
nome: "Nome da Extensão"
slug: "nome-extensao"
versao: "1.0"
comando: "/nome"
status: "ativo"
descricao: |
  Descrição detalhada do que a extensão faz,
  para quem é e quais resultados entrega.

# Agentes (mínimo 1)
agentes:
  - id: agente-1
    arquivo: agentes/AGENTE-1.md
    comando: /comando-1
    especialidades:
      - Especialidade 1
      - Especialidade 2
      - Especialidade 3

  - id: agente-2
    arquivo: agentes/AGENTE-2.md
    comando: /comando-2
    especialidades:
      - Especialidade A
      - Especialidade B

# Tarefas (mínimo 1)
tarefas:
  - fase: descoberta
    comando: /tarefa-1
    arquivo: tarefas/tarefa-1.yaml
    agente: agente-1
    descricao: O que faz

  - fase: criacao
    comando: /tarefa-2
    arquivo: tarefas/tarefa-2.yaml
    agente: agente-2
    descricao: O que faz

# Workflows (mínimo 1)
workflows:
  - id: workflow-principal
    comando: /workflow-completo
    arquivo: workflows/workflow-principal.yaml
    descricao: Processo completo

  - id: modo-iniciante
    comando: /iniciante-nome
    arquivo: workflows/modo-iniciante.yaml
    descricao: Versão rápida
    integracao: ralph

# Conhecimento (mínimo 1)
conhecimento:
  - tema-1.md
  - tema-2.md
  - tema-3.md

# Referências (opcional)
referencias:
  area_1:
    - Referência 1
    - Referência 2
  area_2:
    - Referência A
    - Referência B

# Integrações (opcional)
integracoes:
  ralph:
    ativo: true
    templates:
      - prd-nome.json
      - prompt-nome.md

  outras_extensoes:
    - nome: marketing
      uso: "Para criar páginas de vendas"

# Output
output:
  tipo_1: output/tipo-1/
  tipo_2: output/tipo-2/

projetos: projetos/nome-[projeto]/
```

### Campos Obrigatórios

| Campo | Tipo | Descrição |
|-------|------|-----------|
| nome | string | Nome legível da extensão |
| slug | string | Identificador único (kebab-case) |
| versao | string | Versão semântica |
| comando | string | Comando para ativar |
| status | string | "ativo" ou "inativo" |
| descricao | string | Descrição detalhada |
| agentes | array | Lista de agentes |
| tarefas | array | Lista de tarefas |
| conhecimento | array | Arquivos de conhecimento |

### Campos Opcionais

| Campo | Tipo | Descrição |
|-------|------|-----------|
| workflows | array | Workflows disponíveis |
| referencias | object | Referências e mestres |
| integracoes | object | Integrações com Ralph e outras |
| output | object | Diretórios de saída |
| projetos | string | Padrão de projetos |

## Componentes da Extensão

### 1. Agentes

Cada extensão deve ter **pelo menos 1 agente**, idealmente **3 agentes** que se complementam:

| Papel | Descrição | Exemplo |
|-------|-----------|---------|
| **Estrategista** | Visão, planejamento | Estrategista de Marketing |
| **Executor** | Criação, produção | Copywriter |
| **Avaliador** | Qualidade, métricas | Especialista em Avaliação |

### 2. Tarefas

Tarefas são ações específicas que os agentes executam:

- **Mínimo:** 1 tarefa
- **Ideal:** 5-10 tarefas
- **Organizadas por fase:** descoberta, criação, avaliação, etc.

### 3. Workflows

Workflows são processos completos que orquestram múltiplas tarefas:

| Tipo | Descrição | Característica |
|------|-----------|----------------|
| **Modo Iniciante** | Rápido, 5 perguntas | Integração com Ralph |
| **Modo Completo** | Profissional, detalhado | Múltiplas fases |
| **Workflows Rápidos** | Tarefas específicas | Foco único |

### 4. Conhecimento

Base de conhecimento com metodologias e referências:

- Frameworks e metodologias
- Boas práticas
- Referências e mestres
- Templates e exemplos

## Convenções de Nomenclatura

### Extensão

| Elemento | Padrão | Exemplo |
|----------|--------|---------|
| Diretório | kebab-case | `extensoes/educacional/` |
| Nome | Title Case | "Educacional" |
| Slug | kebab-case | "educacional" |
| Comando | /slug | "/educacional" |

### Agentes

| Elemento | Padrão | Exemplo |
|----------|--------|---------|
| Arquivo | MAIÚSCULAS-COM-HÍFEN.md | `DESIGNER-INSTRUCIONAL.md` |
| ID | kebab-case | "designer-instrucional" |
| Comando | /comando | "/design-instrucional" |

### Tarefas

| Elemento | Padrão | Exemplo |
|----------|--------|---------|
| Arquivo | kebab-case.yaml | `criar-aula.yaml` |
| ID | kebab-case | "criar-aula" |
| Comando | /verbo-objeto | "/criar-aula" |

### Workflows

| Elemento | Padrão | Exemplo |
|----------|--------|---------|
| Arquivo | kebab-case.yaml | `curso-completo.yaml` |
| ID | kebab-case | "curso-completo" |
| Comando | /nome | "/curso-completo" |

## Integração com Sistema

### delegacao.yaml

Toda extensão deve ser registrada em `core/orquestrador/delegacao.yaml`:

```yaml
extensao_[nome]:
  agente_1:
    agente: extensoes/[nome]/agentes/AGENTE-1.md
    gatilhos:
      - "gatilho 1"
      - "gatilho 2"
    tarefas:
      - tarefa-1
      - tarefa-2
```

### CLAUDE.md

Toda extensão deve ser adicionada em `.claude/CLAUDE.md`:

1. Na tabela de extensões
2. Nos modos de trabalho (se tiver workflow)
3. No comportamento padrão

### Output

Criar diretórios de saída em `output/`:

```bash
output/
├── [tipo-1]/
├── [tipo-2]/
└── [tipo-3]/
```

## Checklist de Extensão Completa

### Estrutura ✓
- [ ] Diretório criado em `extensoes/`
- [ ] `extensao.yaml` válido
- [ ] `README.md` documentado
- [ ] Diretórios internos: agentes/, conhecimento/, tarefas/, workflows/

### Agentes ✓
- [ ] Mínimo 1 agente criado
- [ ] Identidade definida
- [ ] Especialidades listadas
- [ ] Regras documentadas
- [ ] Processo de trabalho

### Tarefas ✓
- [ ] Mínimo 1 tarefa criada
- [ ] Entradas definidas
- [ ] Passos documentados
- [ ] Template de saída
- [ ] Gates de qualidade

### Workflows ✓
- [ ] Mínimo 1 workflow
- [ ] Fases documentadas
- [ ] Etapas com entregáveis
- [ ] Checkpoints definidos
- [ ] Entrega final especificada

### Conhecimento ✓
- [ ] Base de conhecimento criada
- [ ] Referências documentadas
- [ ] Metodologias explicadas

### Integração ✓
- [ ] `delegacao.yaml` atualizado
- [ ] `CLAUDE.md` atualizado
- [ ] Pastas de output criadas
- [ ] Templates Ralph (se aplicável)

## Exemplos de Extensões

### Marketing
- **Agentes:** Copywriter, Estrategista, Tráfego
- **Tarefas:** criar-headline, criar-email, criar-oferta
- **Workflows:** oferta-completa, lancamento, modo-iniciante

### Educacional
- **Agentes:** Designer Instrucional, Conteudista, Especialista Avaliação
- **Tarefas:** estruturar-curso, criar-aula, criar-atividade
- **Workflows:** curso-completo, modo-iniciante-curso

### Branding
- **Agentes:** Designer, UI/UX, Brand Strategist
- **Tarefas:** criar-logo, paleta-cores, design-system
- **Workflows:** brand-completo, identidade-visual
