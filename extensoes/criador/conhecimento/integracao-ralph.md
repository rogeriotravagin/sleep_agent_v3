# Integração com Ralph - Base de Conhecimento

## O que é o Ralph

Ralph é o sistema de execução autônoma do Sleep Agent. Ele recebe um PRD (Product Requirements Document) e itera automaticamente até completar todas as user stories.

## Quando Usar Ralph

### ✅ Usar Ralph Para
- Geração de múltiplos arquivos
- Tarefas repetitivas estruturadas
- Workflows de modo iniciante
- Criação de estruturas completas

### ❌ Não Usar Ralph Para
- Tarefas simples e pontuais
- Interações que requerem muita decisão humana
- Trabalhos criativos únicos
- Análises que precisam de contexto dinâmico

## Componentes da Integração

### 1. PRD (Product Requirements Document)

```json
{
  "metadata": {
    "type": "tipo-do-projeto",
    "version": "1.0",
    "created_by": "Sleep Agent"
  },
  "project": {
    "name": "{{nome}}",
    "slug": "{{slug}}",
    "description": "{{descricao}}"
  },
  "user_stories": [
    {
      "id": "US001",
      "title": "Título da User Story",
      "description": "Como [persona], quero [ação] para [benefício]",
      "acceptance_criteria": [
        "Critério 1",
        "Critério 2"
      ],
      "priority": "high",
      "deliverables": [
        "arquivo1.md",
        "arquivo2.md"
      ]
    }
  ],
  "quality_gates": {
    "categoria": [
      "Pergunta de validação?"
    ]
  },
  "knowledge_base": [
    "caminho/para/conhecimento.md"
  ],
  "output_structure": {
    "base_path": "output/{{tipo}}/",
    "directories": ["dir1", "dir2"]
  }
}
```

### 2. Prompt

```markdown
# Prompt para Ralph - [Tipo de Projeto]

## Contexto
[Descrição do que será feito]

### Informações do Projeto
- **Nome:** {{nome}}
- **Tema:** {{tema}}
- **Público:** {{publico}}

---

## Base de Conhecimento
[Resumo das metodologias e referências]

---

## User Stories para Execução

### US001: [Título]
[Descrição detalhada]

**Critérios de Aceitação:**
- [ ] Critério 1
- [ ] Critério 2

**Entregáveis:**
- arquivo1.md
- arquivo2.md

---

## Regras de Qualidade
[Gates e validações]

---

## Checklist de Conclusão
- [ ] Item 1
- [ ] Item 2

---

## Início da Execução
[Instruções de como começar]
```

## Estrutura de User Stories

### Formato Padrão

```yaml
user_story:
  id: "US001"
  title: "Título curto e descritivo"
  description: "Como [persona], quero [ação] para [benefício]"
  acceptance_criteria:
    - "Critério mensurável 1"
    - "Critério mensurável 2"
    - "Critério mensurável 3"
  priority: "high|medium|low"
  deliverables:
    - "caminho/para/arquivo1.md"
    - "caminho/para/arquivo2.md"
```

### Boas Práticas

**Título:**
- Verbo no infinitivo
- Descritivo do resultado
- Máximo 10 palavras

**Descrição:**
- Formato: Como [quem], quero [o quê] para [por quê]
- Clara e específica
- Foco no benefício

**Critérios de Aceitação:**
- Mensuráveis e verificáveis
- 3-5 critérios por story
- Específicos, não vagos

**Prioridade:**
- `high`: Essencial, fazer primeiro
- `medium`: Importante, depois das high
- `low`: Desejável, se houver tempo

### Exemplos por Tipo

**Criação de Conteúdo:**
```yaml
- id: "US001"
  title: "Criar estrutura completa do curso"
  description: "Como criador de curso, quero uma estrutura organizada para desenvolver o conteúdo"
  acceptance_criteria:
    - "Grade curricular completa"
    - "Objetivos por módulo"
    - "Sequência lógica"
  priority: "high"
  deliverables:
    - "estrutura/grade-curricular.md"
```

**Geração de Arquivos:**
```yaml
- id: "US002"
  title: "Criar planos de aula"
  description: "Como criador, quero planos detalhados de cada aula"
  acceptance_criteria:
    - "Hook de abertura"
    - "Conteúdo estruturado"
    - "Exercício prático"
  priority: "high"
  deliverables:
    - "aulas/modulo-{{n}}/aula-{{n}}-{{m}}.md"
```

## Configuração no Workflow

### No extensao.yaml

```yaml
integracoes:
  ralph:
    ativo: true
    templates:
      - prd-[tipo].json
      - prompt-[tipo].md
    scripts:
      - ralph-[tipo].sh
```

### No Workflow

```yaml
fases:
  - numero: 3
    nome: PREPARAR RALPH
    automatico: true

    etapas:
      - id: montar-prd
        nome: "Montar PRD"
        automatico: true
        entregavel: prd.json

      - id: gerar-prompt
        nome: "Gerar Prompt"
        automatico: true
        entregavel: prompt.md

  - numero: 4
    nome: EXECUTAR RALPH

    execucao:
      comando: "./frameworks/ralph/scripts/ralph.sh 30"
      parametros:
        prd: "{{prd_path}}"
        output: "{{output_path}}"
        max_iteracoes: 30

ralph:
  template_prd: frameworks/ralph/templates/prd-[tipo].json
  template_prompt: frameworks/ralph/templates/prompt-[tipo].md
  configuracao:
    max_iteracoes: 30
    paralelismo: false
    validacao: true
```

## Criando Templates Ralph

### Passo 1: Definir User Stories

1. Listar todos os entregáveis necessários
2. Agrupar em user stories lógicas
3. Definir critérios de aceitação
4. Estabelecer prioridades

### Passo 2: Criar PRD

```json
{
  "metadata": {
    "type": "[tipo]",
    "version": "1.0"
  },
  "project": {
    "name": "{{nome}}",
    "slug": "{{slug}}"
  },
  "user_stories": [
    // ... user stories definidas
  ],
  "quality_gates": {
    // ... validações por categoria
  },
  "knowledge_base": [
    // ... arquivos de conhecimento
  ],
  "output_structure": {
    "base_path": "output/[tipo]/{{slug}}/",
    "directories": [
      // ... diretórios a criar
    ]
  }
}
```

### Passo 3: Criar Prompt

```markdown
# Prompt para Ralph - [Tipo]

## Contexto
[O que será feito]

## Base de Conhecimento
[Metodologias e referências]

## User Stories
[Detalhamento de cada story]

## Regras
[Validações e qualidade]

## Execução
[Como começar]
```

### Passo 4: Testar

```bash
# Testar geração
./frameworks/ralph/scripts/ralph.sh 5  # Poucas iterações para teste

# Validar saída
# Ajustar PRD/Prompt se necessário

# Executar completo
./frameworks/ralph/scripts/ralph.sh 30
```

## Localização dos Templates

```
frameworks/ralph/templates/
├── prd.json                    # Template genérico
├── prd-pagina-vendas.json      # Marketing
├── prd-curso.json              # Educacional
├── prd-extensao.json           # Criador
├── prompt.md                   # Prompt genérico
├── prompt-pagina-vendas.md     # Marketing
├── prompt-curso.md             # Educacional
└── prompt-extensao.md          # Criador
```

## Comandos Ralph

```bash
# Execução simples
./frameworks/ralph/scripts/ralph.sh [max_iteracoes]

# Execução paralela
./frameworks/ralph/scripts/ralph-parallel.sh [num_paralelo]

# Execução em swarm
./frameworks/ralph/scripts/ralph-swarm.sh
```

## Checklist de Integração

- [ ] PRD template criado
- [ ] Prompt template criado
- [ ] User stories definidas (mínimo 5)
- [ ] Critérios de aceitação claros
- [ ] Knowledge base referenciado
- [ ] Output structure definido
- [ ] Workflow configurado
- [ ] Teste realizado
