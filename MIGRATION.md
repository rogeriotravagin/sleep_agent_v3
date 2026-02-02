# AIOS → Sleep Agent Framework (SAF) - Migration Map

**Data:** 2026-02-01
**Objetivo:** Documentar todas as referências ao AIOS Framework para remoção segura

---

## Executive Summary

| Métrica | Valor |
|---------|-------|
| **Total de ocorrências** | ~120+ |
| **Arquivos afetados** | ~50 arquivos |
| **Áreas principais** | frameworks/ralph/, extensoes/marketing/, extensoes/dados/ |
| **Criticidade** | Alta (afeta documentação core) |

---

## Categorização por Tipo

### 1. Referências CRÍTICAS (Funcionalidade)

| Arquivo | Linha | Contexto | Ação |
|---------|-------|----------|------|
| `frameworks/ralph/config.yaml` | 2 | `# AIOS-FULLSTACK Compliant` | Substituir por `# SAF Compliant` |
| `frameworks/ralph/config.yaml` | 7-8 | author field | Substituir por `Sleep Agent Team` |
| `frameworks/ralph/templates/prompt.md` | 3,20,75,251 | Princípios core | Substituir `AIOS` por `SAF` |
| `frameworks/ralph/agents/ralph.md` | 54,66,200 | Agent delegation | Substituir |
| `frameworks/ralph/checklists/quality-gates.md` | 6,15,207,209 | Quality gates | Substituir |

### 2. Referências em DOCUMENTAÇÃO

| Arquivo | Ocorrências | Tipo |
|---------|-------------|------|
| `frameworks/ralph/README.md` | 23 | Documentação principal |
| `frameworks/ralph/templates/prd-template.md` | 4 | Template core |
| `frameworks/ralph/workflows/autonomous-loop.md` | 3 | Workflow docs |
| `frameworks/ralph/data/agent-delegation.md` | 2 | Delegation docs |
| `frameworks/ralph/checklists/pre-implementation.md` | 2 | Checklist docs |

### 3. Referências em EXTENSÕES

#### extensoes/marketing/
| Arquivo | Ocorrências | Crítico? |
|---------|-------------|----------|
| `config.yaml` | 2 | ✅ Sim |
| `projects/copy-workflows-yolo/*` | 15+ | ⚠️ Médio |
| `tasks/*.md` | 4 | ⚠️ Médio |
| `templates/*.yaml` | 8 | ⚠️ Médio |
| `README.md` | 1 | ⚠️ Médio |

#### extensoes/dados/
| Arquivo | Ocorrências | Crítico? |
|---------|-------------|----------|
| `config.yaml` | 2 | ✅ Sim |
| `agents/data-chief.md` | 1 | ⚠️ Médio |

#### extensoes/criminal/
| Arquivo | Ocorrências | Crítico? |
|---------|-------------|----------|
| `prompt.md` | 1 | ⚠️ Médio |

### 4. Referências COSMÉTICAS (Comentários)

| Padrão | Substituição |
|--------|--------------|
| `> **AIOS Integration:**` | `> **SAF Integration:**` |
| `> **AIOS Principle:**` | `> **SAF Principle:**` |
| `# AIOS-FULLSTACK Compliant` | `# SAF Compliant` |
| `author: AIOS Framework` | `author: Sleep Agent Framework` |
| `author: "AIOS Team"` | `author: "Sleep Agent Team"` |

---

## Plano de Substituição

### Fase 1: frameworks/ralph/ (CRÍTICO)
```bash
frameworks/ralph/
├── README.md                     ✅ 23 substituições
├── config.yaml                   ✅ 4 substituições
├── agents/ralph.md               ✅ 3 substituições
├── checklists/
│   ├── quality-gates.md         ✅ 4 substituições
│   └── pre-implementation.md    ✅ 2 substituições
├── templates/
│   ├── prompt.md                ✅ 4 substituições
│   ├── prd-template.md          ✅ 4 substituições
│   ├── progress.txt             ✅ 4 substituições
│   └── *.json                   ✅ ~8 arquivos
├── tasks/                        ✅ 6 arquivos
├── workflows/
│   └── autonomous-loop.md       ✅ 3 substituições
└── data/
    └── agent-delegation.md       ✅ 2 substituições
```

### Fase 2: extensoes/ (MÉDIO)
```bash
extensoes/marketing/frameworks/copy/
├── config.yaml                   ⚠️ 2 substituições
├── README.md                     ⚠️ 1 substituição
├── projects/                     ⚠️ ~30 substituições
├── tasks/                        ⚠️ 4 arquivos
└── templates/                    ⚠️ 8 arquivos

extensoes/dados/frameworks/data/
├── config.yaml                   ⚠️ 2 substituições
└── agents/data-chief.md          ⚠️ 1 substituição

extensoes/criminal/
└── prompt.md                     ⚠️ 1 substituição
```

---

## Substituições Detalhadas

### String Replacements

| De | Para |
|----|------|
| `AIOS Framework` | `Sleep Agent Framework (SAF)` |
| `AIOS Integration` | `SAF Integration` |
| `AIOS Principle` | `SAF Principle` |
| `AIOS-Compliant` | `SAF-Compliant` |
| `AIOS-Enhanced` | `SAF-Enhanced` |
| `AIOS-FULLSTACK` | `SAF-FULLSTACK` |
| `aios-core` | `saf-core` |
| `aios-artifacts` | `saf-artifacts` |
| `author: AIOS Framework` | `author: Sleep Agent Framework` |
| `author: "AIOS Team"` | `author: "Sleep Agent Team"` |
| `author: AIOS Ralph` | `author: Sleep Agent Ralph` |
| `@AIOS` | `@SAF` |

### URL/Path Replacements

| De | Para |
|----|------|
| `.aios-core/` | `.saf-core/` ou remover link |
| `aios-artifacts` (category) | `saf-artifacts` |

---

## Arquivos para REMOVER/ARQUIVAR

| Arquivo | Ação | Razão |
|---------|------|-------|
| Nenhum | - | Todos os conceitos serão mantidos |

---

## Validação Pós-Migração

### Comandos de Validação

```bash
# 1. Verificar que não há mais referências AIOS
grep -rn "AIOS\|aios" --include="*.md" --include="*.yaml" --include="*.json" \
  frameworks/ extensoes/ --exclude-dir=node_modules 2>/dev/null

# Resultado esperado: 0 ocorrências (exceto este arquivo MIGRATION.md)

# 2. Verificar que Ralph ainda funciona
cd frameworks/ralph/
ls -la *.md *.yaml

# 3. Verificar sintaxe YAML
yamllint frameworks/ralph/config.yaml
yamllint extensoes/*/config.yaml

# 4. Verificar sintaxe JSON
jq . frameworks/ralph/templates/*.json
```

### Checklist de Validação

- [ ] Zero ocorrências de "AIOS" (grep retorna vazio)
- [ ] Arquivos YAML válidos (yamllint passa)
- [ ] Arquivos JSON válidos (jq valida)
- [ ] README.md legível e coerente
- [ ] Documentação SAF criada
- [ ] Ralph pode ser ativado (@ralph)
- [ ] Quality gates funcionam
- [ ] Handoff system funciona
- [ ] Templates carregam corretamente

---

## Riscos e Mitigações

| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|-----------|
| Quebrar funcionalidade Ralph | Baixo | Alto | Testar após cada fase |
| Sintaxe YAML incorreta | Médio | Médio | Validar com yamllint |
| Referências perdidas | Baixo | Baixo | Grep final |
| Documentação inconsistente | Médio | Baixo | Review manual |

---

## Referências

- **AIOS Original:** (removido por questões legais)
- **Sleep Agent Framework:** Documentação própria a ser criada
- **Princípios mantidos:** Story-Driven, Quality Gates, Handoff System, Agent Delegation, Patterns Compound

---

## Status

✅ **US-001 COMPLETO** - Mapeamento criado
⏳ **Próximo:** US-002 - Definir terminologia SAF
