# Extensao Criminal - Sleep Agent

## Visao Geral

Framework especializado em Direito Penal brasileiro para advogados criminalistas. Oferece agentes especializados para cada fase do processo criminal, desde a defesa inicial ate a execucao penal.

---

## Disclaimer

**AVISO IMPORTANTE**: Esta extensao foi desenvolvida para auxiliar advogados criminalistas na elaboracao de pecas processuais. Todos os documentos gerados sao para fins de orientacao e **DEVEM SER REVISADOS** por advogado inscrito na OAB antes de utilizacao em processos reais.

A responsabilidade pela utilizacao do conteudo e exclusivamente do profissional que o apresentar em juizo.

---

## Instalacao

A extensao ja vem instalada no Sleep Agent. Para verificar se esta disponivel:

```
/extensoes
```

---

## Comando de Ativacao

```
/criminal
```

Ao ativar, o sistema carrega os agentes especializados e disponibiliza todos os comandos da extensao.

---

## Agentes Disponiveis

| Agente | Comando | Especialidade |
|--------|---------|---------------|
| Criminalista | `/defesa` | Defesa criminal em geral, teses, dosimetria |
| Especialista em Juri | `/juri` | Crimes dolosos contra a vida, plenario |
| Especialista em Execucao | `/execucao` | Progressao, livramento, beneficios |
| Especialista em Recursos | `/recursos` | HC, apelacao, pedidos de liberdade |

---

## Tarefas Disponiveis

### Analise Inicial
| Comando | Descricao |
|---------|-----------|
| `/parecer-criminal` | Analisar viabilidade da defesa |
| `/tese-defesa` | Desenvolver tese de defesa |

### Defesa Preliminar
| Comando | Descricao |
|---------|-----------|
| `/resposta-acusacao` | Resposta a acusacao (art. 396 CPP) |
| `/pedido-liberdade` | Liberdade provisoria |
| `/relaxamento` | Relaxamento de prisao ilegal |
| `/revogacao-preventiva` | Revogacao de prisao preventiva |

### Instrucao e Julgamento
| Comando | Descricao |
|---------|-----------|
| `/alegacoes-finais` | Alegacoes finais por memoriais |
| `/quesitos-juri` | Quesitos para Tribunal do Juri |

### Recursos
| Comando | Descricao |
|---------|-----------|
| `/habeas-corpus` | Habeas corpus |
| `/apelacao` | Apelacao criminal |
| `/agravo-execucao` | Agravo em execucao penal |

### Execucao Penal
| Comando | Descricao |
|---------|-----------|
| `/pedido-progressao` | Progressao de regime |

---

## Workflows

Workflows sao fluxos completos que combinam multiplas tarefas:

### 1. Defesa Completa (`/defesa-completa`)
Estrategia de defesa do inicio ao fim:
- Analise dos autos
- Identificacao de nulidades
- Definicao de tese
- Elaboracao de pecas

### 2. Liberdade (`/liberdade`)
Obter liberdade do cliente:
- Avaliacao da situacao prisional
- Escolha da medida adequada (HC, relaxamento, revogacao)
- Elaboracao da peca

### 3. Progressao (`/progressao`)
Pedido de progressao de regime:
- Calculo de requisitos temporais
- Verificacao de requisitos subjetivos
- Elaboracao do pedido

---

## Base de Conhecimento

A extensao inclui conhecimento especializado em:

| Arquivo | Conteudo |
|---------|----------|
| `codigo-penal.md` | Codigo Penal - crimes e penas |
| `codigo-processo-penal.md` | CPP - procedimentos e recursos |
| `execucao-penal.md` | LEP - beneficios da execucao |
| `leis-especiais.md` | Drogas, hediondos, Maria da Penha, etc |
| `sumulas-stf.md` | Sumulas vinculantes e em materia penal |

---

## Legislacao Coberta

### Legislacao Principal
- **Codigo Penal** - Decreto-Lei 2.848/1940
- **Codigo de Processo Penal** - Decreto-Lei 3.689/1941
- **Lei de Execucao Penal** - Lei 7.210/1984
- **Constituicao Federal** - Art. 5o (garantias fundamentais)

### Leis Especiais
- **Lei de Drogas** - Lei 11.343/2006
- **Crimes Hediondos** - Lei 8.072/1990
- **Lei Maria da Penha** - Lei 11.340/2006
- **CTB** - Lei 9.503/1997 (crimes de transito)
- **Crimes Tributarios** - Lei 8.137/1990
- **Lavagem de Dinheiro** - Lei 9.613/1998
- **Estatuto do Desarmamento** - Lei 10.826/2003
- **Organizacoes Criminosas** - Lei 12.850/2013

### Jurisprudencia
- Sumulas Vinculantes STF
- Sumulas STF em materia penal
- Sumulas STJ (5a e 6a Turmas)
- Jurisprudencia em Teses STJ

---

## Estrutura de Arquivos

```
extensoes/criminal/
├── .claude/
│   └── CLAUDE.md              # Instrucoes especificas da extensao
├── core/
│   └── orquestrador/
│       └── delegacao.yaml     # Regras de delegacao
├── agentes/
│   ├── CRIMINALISTA.md        # Agente de defesa geral
│   ├── JURI.md                # Especialista em juri
│   ├── EXECUCAO.md            # Especialista em execucao
│   └── RECURSOS.md            # Especialista em recursos
├── conhecimento/
│   ├── codigo-penal.md        # CP resumido
│   ├── codigo-processo-penal.md # CPP resumido
│   ├── execucao-penal.md      # LEP resumida
│   ├── leis-especiais.md      # Leis penais especiais
│   └── sumulas-stf.md         # Sumulas em materia penal
├── tarefas/
│   ├── resposta-acusacao.yaml
│   ├── alegacoes-finais.yaml
│   ├── habeas-corpus.yaml
│   ├── apelacao.yaml
│   ├── pedido-liberdade.yaml
│   ├── relaxamento.yaml
│   ├── revogacao-preventiva.yaml
│   ├── pedido-progressao.yaml
│   ├── agravo-execucao.yaml
│   └── quesitos-juri.yaml
├── workflows/
│   ├── defesa-completa.yaml
│   ├── liberdade.yaml
│   └── progressao.yaml
├── extensao.yaml              # Manifesto da extensao
└── README.md                  # Esta documentacao
```

---

## Uso Basico

### Exemplo 1: Elaborar Resposta a Acusacao

```
/criminal
/resposta-acusacao
```

O agente ira perguntar:
1. Qual o crime imputado?
2. Quais os fatos narrados na denuncia?
3. O cliente esta preso ou em liberdade?
4. Existem nulidades aparentes?
5. O cliente tem antecedentes?

### Exemplo 2: Habeas Corpus Urgente

```
/criminal
/habeas-corpus
```

O agente ira perguntar:
1. Qual a autoridade coatora?
2. Qual o fundamento da prisao?
3. Por que a prisao e ilegal ou abusiva?
4. Ha excesso de prazo?
5. Existem medidas cautelares alternativas viaveis?

### Exemplo 3: Pedido de Progressao

```
/criminal
/pedido-progressao
```

O agente ira perguntar:
1. Qual o regime atual de cumprimento?
2. Qual a data de inicio do cumprimento?
3. Qual a pena total e quanto ja foi cumprido?
4. Ha faltas disciplinares?
5. Trabalha ou estuda (remicao)?
6. Tem laudo de bom comportamento?

---

## Prazos Processuais

| Peca | Prazo | Fundamento |
|------|-------|------------|
| Resposta a acusacao | 10 dias | Art. 396 CPP |
| Alegacoes finais (escrita) | 5 dias | Art. 403 CPP |
| Apelacao criminal | 5 dias | Art. 593 CPP |
| RESE | 5 dias | Art. 586 CPP |
| Embargos de declaracao | 2 dias | Art. 382 CPP |
| Habeas corpus | Sem prazo | - |
| Agravo em execucao | 5 dias | Art. 197 LEP |

---

## Organizacao de Outputs

Os documentos gerados sao salvos em:

```
workspace/[estrutura]/criminal/[tipo]/
```

### Tipos de Pastas
- `pareceres/` - Analises e pareceres
- `defesa/` - Pecas de defesa (resposta, alegacoes)
- `recursos/` - Recursos e HC
- `execucao/` - Pedidos de execucao penal
- `estrategias/` - Documentos estrategicos

---

## Principios Norteadores

Esta extensao segue os principios constitucionais da defesa criminal:

1. **Presuncao de inocencia** (art. 5o, LVII, CF)
2. **Ampla defesa** (art. 5o, LV, CF)
3. **Contraditorio** (art. 5o, LV, CF)
4. **Devido processo legal** (art. 5o, LIV, CF)
5. **In dubio pro reo** - Na duvida, absolve-se
6. **Favor rei** - Interpretacao mais favoravel ao reu
7. **Vedacao de provas ilicitas** (art. 5o, LVI, CF)
8. **Intranscendencia da pena** (art. 5o, XLV, CF)

---

## Contribuicao

Para contribuir com a extensao Criminal:

### Adicionar Nova Tese de Defesa
1. Editar `conhecimento/teses-defesa.md` (quando criado)
2. Incluir fundamentacao juridica
3. Adicionar jurisprudencia de suporte

### Adicionar Nova Tarefa
1. Criar arquivo em `tarefas/nova-tarefa.yaml`
2. Registrar em `extensao.yaml`
3. Adicionar gatilhos em `core/orquestrador/delegacao.yaml`

### Atualizar Jurisprudencia
1. Editar arquivos em `conhecimento/`
2. Manter formato consistente
3. Incluir numero do acordao/sumula

### Reportar Problemas
1. Verificar se e problema de interpretacao juridica
2. Documentar o caso de uso
3. Sugerir correcao com fundamentacao

---

## Versao

**Versao atual:** 1.0

**Changelog:**
- 1.0 - Versao inicial com 4 agentes e 12 tarefas

---

## Suporte

Para duvidas sobre uso da extensao, digite:

```
/ajuda
```

Para duvidas especificas sobre Direito Penal, consulte a base de conhecimento ou um advogado especializado.
