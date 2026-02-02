# Prompt para Extensao Criminal

## Contexto

Voce esta completando a **Extensao Criminal** do Sleep Agent, um framework de agentes para advogados criminalistas. A extensao ja tem a estrutura base criada.

## Arquivos Existentes

```
extensoes/criminal/
├── extensao.yaml          # Manifesto da extensao
├── .claude/CLAUDE.md      # Instrucoes especificas
├── agentes/
│   ├── CRIMINALISTA.md    # Defesa criminal geral
│   ├── JURI.md            # Tribunal do Juri
│   ├── EXECUCAO.md        # Execucao penal
│   └── RECURSOS.md        # Recursos e HC
└── tarefas/
    └── resposta-acusacao.yaml  # Unica tarefa criada
```

## Sua Missao

Completar a extensao criando:
1. **Tarefas** - Arquivos YAML para cada tipo de peca processual
2. **Workflows** - Fluxos de trabalho completos
3. **Conhecimento** - Base de conhecimento juridico
4. **Core** - Regras de orquestracao

## Referencias de Estrutura

Use como modelo:
- `extensoes/marketing/` - Estrutura de extensao
- `extensoes/criminal/tarefas/resposta-acusacao.yaml` - Modelo de tarefa

## Legislacao Base

- **Codigo Penal** - Decreto-Lei 2.848/1940
- **Codigo de Processo Penal** - Decreto-Lei 3.689/1941
- **Lei de Execucao Penal** - Lei 7.210/1984
- **Lei de Drogas** - Lei 11.343/2006
- **Crimes Hediondos** - Lei 8.072/1990
- **Lei Maria da Penha** - Lei 11.340/2006
- **Pacote Anticrime** - Lei 13.964/2019

## Princípios SAF

1. **Story-Driven** - Cada story tem todo contexto necessario
2. **Quality Gates** - Validar antes de marcar como completo
3. **No Scope Creep** - Stick to acceptance criteria
4. **Patterns Compound** - Reusar padroes entre stories

## Disclaimer Obrigatorio

Toda peca ou documento deve incluir ao final:

```
---
**AVISO IMPORTANTE**: Este documento foi gerado com auxilio de inteligencia
artificial para fins de orientacao juridica. E OBRIGATORIA a revisao por
advogado inscrito na OAB antes de utilizacao em processos reais.
---
```

## Qualidade Esperada

- Artigos de lei citados corretamente
- Prazos processuais corretos
- Jurisprudencia relevante (STF/STJ)
- Estrutura de pecas conforme praxe forense
- Linguagem tecnico-juridica adequada
