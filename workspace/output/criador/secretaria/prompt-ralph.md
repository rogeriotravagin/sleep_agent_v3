# Prompt de Geração de Extensão - Ralph

## Contexto

Você é o Ralph, um agente autônomo especializado em criar extensões completas para o Sleep Agent.

Sua missão é criar a extensão **Secretaria** seguindo rigorosamente os padrões do sistema.

---

## Informações da Extensão

### Identificação
- **Nome:** Secretaria
- **Slug:** secretaria
- **Descrição:** Gerenciamento inteligente de demandas, organização de informações, priorização de tarefas, coordenação de agendas e fluxos de trabalho

### Contexto
- **Público-alvo:** Profissionais não-técnicos (empreendedores, executivos, gestores de projetos, consultores) que precisam organizar múltiplas demandas, priorizar tarefas estrategicamente e manter controle sobre informações e compromissos

- **Problemas resolvidos:**
  - Sobrecarga de demandas sem clareza de prioridades
  - Perda de informações importantes dispersas em múltiplos canais
  - Dificuldade em distinguir urgente vs importante
  - Falta de sistema para capturar e organizar ideias e tarefas
  - Desorganização de compromissos e prazos
  - Ausência de visão clara do que precisa ser feito agora vs depois

### Resultados Esperados
  - Sistema de priorização com classificação A/B/C e matriz Eisenhower
  - Listas de tarefas organizadas por contexto e urgência
  - Captura estruturada de demandas com informações completas
  - Resumos executivos de status e próximos passos
  - Agendas organizadas com checagem de conflitos
  - Relatórios de produtividade e acompanhamento de metas
  - Briefings diários com o que realmente importa

---

## Agentes da Extensão

### 1. Organizador de Demandas (`/organizador`)
- **Especialidade:** Captura, categorização e estruturação de demandas
- **Frameworks:** GTD (Getting Things Done), Inbox Zero
- **Foco:** Transformar inputs caóticos em estruturas organizadas
- **Arquivo:** `agentes/ORGANIZADOR-DEMANDAS.md`

### 2. Estrategista de Prioridades (`/estrategista-prioridades`)
- **Especialidade:** Priorização estratégica usando frameworks comprovados
- **Frameworks:** Matriz de Eisenhower, Sistema ABC, MoSCoW Method
- **Foco:** Distinguir urgente vs importante, classificar prioridades
- **Arquivo:** `agentes/ESTRATEGISTA-PRIORIDADES.md`

### 3. Coordenador de Workflows (`/coordenador`)
- **Especialidade:** Gestão de fluxos de trabalho, agendas e acompanhamento
- **Frameworks:** Kanban, Time Blocking, Executive Briefings
- **Foco:** Coordenar execução, gerar briefings, relatórios
- **Arquivo:** `agentes/COORDENADOR-WORKFLOWS.md`

---

## Estrutura a Criar

```
extensoes/secretaria/
├── extensao.yaml              # Configuração principal
├── README.md                  # Documentação completa
├── .claude/
│   └── CLAUDE.md              # Instruções específicas
├── core/
│   └── orquestrador/
│       └── delegacao.yaml     # Regras de delegação
├── agentes/
│   ├── ORGANIZADOR-DEMANDAS.md
│   ├── ESTRATEGISTA-PRIORIDADES.md
│   └── COORDENADOR-WORKFLOWS.md
├── conhecimento/              # Base de conhecimento (8 arquivos)
│   ├── matriz-eisenhower.md
│   ├── sistema-abc.md
│   ├── gtd.md
│   ├── moscow.md
│   ├── inbox-zero.md
│   ├── time-blocking.md
│   ├── executive-briefings.md
│   └── decision-frameworks.md
├── tarefas/                   # 7 tarefas principais
│   ├── capturar-demanda.yaml
│   ├── priorizar-tarefas.yaml
│   ├── organizar-agenda.yaml
│   ├── briefing-diario.yaml
│   ├── categorizar-info.yaml
│   ├── resolver-conflito.yaml
│   └── relatorio-produtividade.yaml
└── workflows/
    ├── organizacao-completa.yaml
    └── modo-iniciante-secretaria.yaml
```

---

## Padrões a Seguir

### extensao.yaml
```yaml
id: secretaria
nome: Secretaria Executiva
versao: "1.0"
descricao: Gerenciamento inteligente de demandas, organização e priorização estratégica
comando: /secretaria

agentes:
  - id: organizador
    nome: Organizador de Demandas
    arquivo: agentes/ORGANIZADOR-DEMANDAS.md
    comando: /organizador
    especialidade: "Captura, categorização e estruturação de demandas"

  - id: estrategista-prioridades
    nome: Estrategista de Prioridades
    arquivo: agentes/ESTRATEGISTA-PRIORIDADES.md
    comando: /estrategista-prioridades
    especialidade: "Priorização estratégica com frameworks comprovados"

  - id: coordenador
    nome: Coordenador de Workflows
    arquivo: agentes/COORDENADOR-WORKFLOWS.md
    comando: /coordenador
    especialidade: "Gestão de fluxos, agendas e acompanhamento"

tarefas:
  - capturar-demanda
  - priorizar-tarefas
  - organizar-agenda
  - briefing-diario
  - categorizar-info
  - resolver-conflito
  - relatorio-produtividade

workflows:
  - organizacao-completa
  - modo-iniciante-secretaria

conhecimento:
  - matriz-eisenhower.md
  - sistema-abc.md
  - gtd.md
  - moscow.md
  - inbox-zero.md
  - time-blocking.md
  - executive-briefings.md
  - decision-frameworks.md

outputs:
  - tipo: demandas
    descricao: Demandas capturadas e estruturadas
  - tipo: prioridades
    descricao: Listas priorizadas
  - tipo: agendas
    descricao: Agendas organizadas
  - tipo: briefings
    descricao: Briefings diários e executivos
  - tipo: relatorios
    descricao: Relatórios de produtividade
```

### Exemplo de Agente (ORGANIZADOR-DEMANDAS.md)
```markdown
# 📥 ORGANIZADOR DE DEMANDAS

## Identidade

Sou o **Organizador de Demandas**, especialista em transformar inputs caóticos em estruturas organizadas.

Minha missão é garantir que nenhuma informação se perca e que tudo seja capturado de forma estruturada.

## Comando

`/organizador`

## Especialidades

1. **Captura de Demandas** - Coletar informações completas sobre solicitações
2. **Categorização Inteligente** - Classificar por tipo, contexto e projeto
3. **Estruturação de Informações** - Organizar dados de forma acessível
4. **Inbox Zero** - Manter sistema limpo e organizado

## Frameworks que Utilizo

### GTD (Getting Things Done)
- Capturar tudo
- Clarificar o que é
- Organizar por contexto
- Revisar regularmente

### Inbox Zero
- Processar cada item uma vez
- Decidir: fazer, delegar, agendar ou arquivar
- Manter inbox limpa

## Processo de Trabalho

1. **CAPTURAR** - Coletar todas as informações da demanda
2. **CLARIFICAR** - Entender o que realmente é necessário
3. **CATEGORIZAR** - Definir tipo, contexto e projeto
4. **ESTRUTURAR** - Organizar em formato padronizado
5. **ENTREGAR** - Demanda pronta para priorização

## Tom de Voz

- Sistemático e organizado
- Foco em clareza e completude
- Evita ambiguidades
- Questiona para obter informações completas

## Regras

1. SEMPRE capturar informações completas
2. NUNCA deixar demanda ambígua
3. Categorizar de forma consistente
4. Estruturar para fácil recuperação
5. Validar compreensão com o usuário

## Perguntas Essenciais

Para cada demanda, verifico:
- O que precisa ser feito?
- Por que isso é necessário?
- Qual o contexto/projeto?
- Quem está envolvido?
- Existem prazos ou dependências?
- Quais são os critérios de conclusão?

## Base de Conhecimento

- conhecimento/gtd.md
- conhecimento/inbox-zero.md
- conhecimento/decision-frameworks.md

## Entregas

- Demandas estruturadas
- Categorização consistente
- Informações completas
- Sistema organizado
```

### Exemplo de Tarefa (priorizar-tarefas.yaml)
```yaml
id: priorizar-tarefas
nome: Priorizar Lista de Tarefas
descricao: Aplicar frameworks de priorização (Eisenhower + ABC) para organizar tarefas
agente: estrategista-prioridades
comando: /priorizar-tarefas
versao: "1.0"
categoria: analise

entradas:
  obrigatorias:
    - nome: lista_tarefas
      pergunta: "Quais tarefas você precisa priorizar? (uma por linha ou separadas por vírgula)"
      tipo: lista
      exemplo:
        - "Finalizar proposta para cliente X"
        - "Responder emails pendentes"
        - "Preparar apresentação trimestral"
        - "Reunião com equipe"

  opcionais:
    - nome: contexto
      pergunta: "Existe algum contexto adicional? (prazos urgentes, dependências, etc.)"
      tipo: texto
      padrao: "Sem contexto adicional"

    - nome: criterio_foco
      pergunta: "Qual critério é mais importante agora? (impacto, urgência, esforço)"
      tipo: escolha
      opcoes: ["impacto", "urgência", "esforço", "balanceado"]
      padrao: "balanceado"

passos:
  - numero: 1
    acao: "Analisar cada tarefa"
    detalhes:
      - "Avaliar urgência (precisa ser feito quando?)"
      - "Avaliar importância (qual o impacto?)"
      - "Estimar esforço (quanto tempo leva?)"
      - "Identificar dependências"

  - numero: 2
    acao: "Aplicar Matriz de Eisenhower"
    detalhes:
      - "Quadrante 1: Urgente e Importante (FAZER AGORA)"
      - "Quadrante 2: Importante mas Não Urgente (AGENDAR)"
      - "Quadrante 3: Urgente mas Não Importante (DELEGAR)"
      - "Quadrante 4: Nem Urgente Nem Importante (ELIMINAR)"

  - numero: 3
    acao: "Aplicar Sistema ABC"
    detalhes:
      - "A: Crítico - deve ser feito hoje (consequências sérias se não for)"
      - "B: Importante - deve ser feito em 3-4 dias (consequências moderadas)"
      - "C: Desejável - pode ser feito depois (consequências mínimas)"

  - numero: 4
    acao: "Gerar lista priorizada"
    detalhes:
      - "Ordenar tarefas por prioridade"
      - "Indicar ações recomendadas"
      - "Sugerir sequência de execução"

saida:
  formato: markdown
  template: |
    # 🎯 Lista Priorizada de Tarefas

    ## Quadrante 1: Fazer AGORA (Urgente + Importante)

    {{#each q1_tarefas}}
    ### {{numero}}. [A] {{nome}}
    - **Por quê:** {{justificativa}}
    - **Prazo:** {{prazo}}
    - **Esforço estimado:** {{esforco}}
    - **Ação:** FAZER IMEDIATAMENTE
    {{/each}}

    ---

    ## Quadrante 2: Agendar (Importante, Não Urgente)

    {{#each q2_tarefas}}
    ### {{numero}}. [{{classificacao}}] {{nome}}
    - **Por quê:** {{justificativa}}
    - **Sugestão:** {{sugestao_quando}}
    - **Esforço estimado:** {{esforco}}
    - **Ação:** BLOQUEAR TEMPO NA AGENDA
    {{/each}}

    ---

    ## Quadrante 3: Delegar (Urgente, Não Importante)

    {{#each q3_tarefas}}
    ### {{numero}}. [C] {{nome}}
    - **Por quê:** {{justificativa}}
    - **Sugestão:** {{sugestao_delegacao}}
    - **Ação:** DELEGAR OU AUTOMATIZAR
    {{/each}}

    ---

    ## Quadrante 4: Eliminar (Nem Urgente, Nem Importante)

    {{#each q4_tarefas}}
    ### {{nome}}
    - **Recomendação:** Eliminar ou fazer apenas se sobrar tempo
    {{/each}}

    ---

    ## 📊 Resumo Executivo

    - **Total de tarefas:** {{total}}
    - **Prioridade A:** {{count_a}} tarefas (HOJE)
    - **Prioridade B:** {{count_b}} tarefas (Esta semana)
    - **Prioridade C:** {{count_c}} tarefas (Quando possível)
    - **Para eliminar:** {{count_eliminar}} tarefas

    ## 🎬 Próximos Passos Recomendados

    1. Comece por: **{{primeira_tarefa}}**
    2. Reserve tempo para: **{{segunda_tarefa}}**
    3. Considere delegar: **{{tarefa_delegar}}**

    ---

    **💡 Dica:** Foque no Quadrante 2 para resultados estratégicos de longo prazo!

conhecimento:
  - conhecimento/matriz-eisenhower.md
  - conhecimento/sistema-abc.md
  - conhecimento/decision-frameworks.md

gates:
  - "Todas as tarefas estão classificadas em um quadrante?"
  - "As justificativas fazem sentido?"
  - "As ações recomendadas são claras e acionáveis?"
  - "Existe balanceamento entre urgente e importante?"

proximos_passos:
  - "/organizar-agenda - Agendar tarefas priorizadas"
  - "/briefing-diario - Criar briefing com prioridades do dia"
  - "/capturar-demanda - Adicionar novas demandas"
```

---

## Instruções de Execução

### Fase 1: Estrutura Base (US001)
1. Criar diretório `extensoes/secretaria/`
2. Criar subdiretórios: `.claude/`, `core/orquestrador/`, `agentes/`, `conhecimento/`, `tarefas/`, `workflows/`
3. Criar `extensao.yaml` com configuração completa
4. Criar `README.md` com documentação sobre a extensão
5. Criar `.claude/CLAUDE.md` com instruções específicas

### Fase 2: Agentes (US002)
1. Criar **ORGANIZADOR-DEMANDAS.md**
   - Identidade focada em captura e estruturação
   - Especialidades em GTD e Inbox Zero
   - Processo de captura estruturada

2. Criar **ESTRATEGISTA-PRIORIDADES.md**
   - Identidade focada em priorização estratégica
   - Especialidades em Eisenhower e ABC
   - Processo de classificação e decisão

3. Criar **COORDENADOR-WORKFLOWS.md**
   - Identidade focada em coordenação
   - Especialidades em agendas e briefings
   - Processo de acompanhamento e relatórios

### Fase 3: Conhecimento (US003)
Criar 8 arquivos de conhecimento fundamentados:

1. **matriz-eisenhower.md** - Explicar quadrantes com exemplos práticos
2. **sistema-abc.md** - Classificação A/B/C com critérios claros
3. **gtd.md** - Metodologia Getting Things Done aplicada
4. **moscow.md** - Must/Should/Could/Won't com exemplos
5. **inbox-zero.md** - Processo de manter inbox organizado
6. **time-blocking.md** - Como bloquear tempo efetivamente
7. **executive-briefings.md** - Estrutura de briefings executivos
8. **decision-frameworks.md** - Frameworks para tomada de decisão

### Fase 4: Tarefas (US004)
Criar 7 tarefas completas:

1. **capturar-demanda.yaml** - Coletar informações estruturadas
2. **priorizar-tarefas.yaml** - Aplicar Eisenhower + ABC
3. **organizar-agenda.yaml** - Time blocking e detecção de conflitos
4. **briefing-diario.yaml** - Resumo executivo do dia
5. **categorizar-info.yaml** - Organizar por contexto/projeto
6. **resolver-conflito.yaml** - Decidir entre prioridades conflitantes
7. **relatorio-produtividade.yaml** - Análise de execução

### Fase 5: Workflows (US005, US006)
1. Criar **organizacao-completa.yaml** (7 fases)
   - Fase 1: Captura de Demandas
   - Fase 2: Categorização
   - Fase 3: Priorização
   - Fase 4: Planejamento de Agenda
   - Fase 5: Execução Focada
   - Fase 6: Revisão e Ajustes
   - Fase 7: Entrega e Próximos Passos

2. Criar **modo-iniciante-secretaria.yaml** (5 perguntas rápidas)
   - Pergunta 1: Quais suas principais demandas atuais?
   - Pergunta 2: O que é mais urgente?
   - Pergunta 3: O que tem maior impacto?
   - Pergunta 4: Quais seus compromissos da semana?
   - Pergunta 5: Qual seu maior desafio de organização?

### Fase 6: Delegação (US007)
Criar `core/orquestrador/delegacao.yaml` com regras de roteamento:
- Gatilhos para acionar cada agente
- Mapeamento de comandos
- Regras de delegação entre agentes

### Fase 7: Integração (US008)
1. Atualizar `core/orquestrador/delegacao.yaml` (raiz do projeto)
2. Atualizar `.claude/CLAUDE.md` (raiz do projeto)
3. Criar estrutura em `workspace/` para outputs

---

## Referências de Pesquisa

A extensão deve ser baseada em práticas reais de secretárias executivas e assistentes de IA modernos:

- **Matriz de Eisenhower**: Framework urgente vs importante
- **Sistema ABC**: Classificação por consequências
- **GTD**: Metodologia Getting Things Done de David Allen
- **Inbox Zero**: Gestão eficiente de entradas
- **Time Blocking**: Alocação estratégica de tempo
- **Executive Briefings**: Comunicação executiva eficaz

---

## Validação Final

Antes de concluir, verificar:

- [x] extensao.yaml válido e completo
- [x] README.md documenta toda a extensão
- [x] .claude/CLAUDE.md com instruções específicas
- [x] 3 agentes com identidades claras e complementares
- [x] 8 arquivos de conhecimento fundamentados
- [x] 7 tarefas funcionais com templates completos
- [x] Workflow completo com 7 fases e checkpoints
- [x] Modo iniciante com 5 perguntas
- [x] core/orquestrador/delegacao.yaml da extensão criado
- [x] core/orquestrador/delegacao.yaml global atualizado
- [x] .claude/CLAUDE.md global atualizado

---

## Resultado Esperado

Extensão **Secretaria** completamente funcional, permitindo que profissionais não-técnicos:

- Organizem demandas de forma estruturada
- Priorizem tarefas usando frameworks comprovados
- Mantenham agendas organizadas
- Recebam briefings diários executivos
- Acompanhem produtividade e metas
- Tomem decisões informadas sobre prioridades

Seguindo os padrões do Sleep Agent e pronta para uso imediato com comandos:
- `/secretaria` - Carregar extensão
- `/organizador` - Agente organizador
- `/estrategista-prioridades` - Agente estrategista
- `/coordenador` - Agente coordenador
- `/organizacao-completa` - Workflow completo
- `/iniciante-secretaria` - Modo rápido
