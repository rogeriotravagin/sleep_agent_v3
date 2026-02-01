# Prompt de Geracao - Extensao Customer Success

## Contexto

Voce e o Ralph, um agente autonomo especializado em criar extensoes completas para o Sleep Agent.

Sua missao e criar a extensao **Customer Success** seguindo rigorosamente os padroes do sistema.

---

## Informacoes da Extensao

### Identificacao
- **Nome:** Customer Success
- **Slug:** customer-success
- **Comando:** /customer-success
- **Descricao:** Extensao completa para gestao de Customer Success, onboarding, retencao e sucesso do cliente

### Contexto
- **Publico-alvo:** Gestores de Customer Success, empreendedores que querem reter mais clientes, times de atendimento e suporte, empresas SaaS, educacao e servicos

### Problemas Resolvidos
- Alto churn de clientes sem acompanhamento adequado
- Onboarding desorganizado que nao gera valor inicial
- Falta de metricas claras de sucesso do cliente
- Clientes insatisfeitos sem acompanhamento proativo
- Dificuldade em criar e mapear jornadas de sucesso
- Ausencia de processos de QBR e review
- Equipe sem playbooks e processos padronizados

### Resultados Esperados
- Playbooks de onboarding estruturados e replicaveis
- Health Score com metricas claras definidas
- Jornadas de sucesso completas mapeadas
- Estrategias de retencao e reducao de churn
- Processos de QBR e Business Review padronizados
- Planos de acao para clientes em risco
- Automacoes de acompanhamento configuradas

---

## Estrutura a Criar

```
extensoes/customer-success/
├── extensao.yaml              # Configuracao principal
├── README.md                  # Documentacao
├── agentes/                   # Agentes especializados
│   ├── CSM-ESTRATEGISTA.md
│   ├── ONBOARDING-SPECIALIST.md
│   └── RETENTION-EXPERT.md
├── conhecimento/              # Base de conhecimento
│   ├── fundamentos-cs.md
│   ├── metricas-cs.md
│   ├── jornada-cliente.md
│   ├── onboarding-framework.md
│   ├── retencao-estrategias.md
│   └── qbr-playbook.md
├── tarefas/                   # Tarefas disponíveis
│   ├── analise-base-clientes.yaml
│   ├── criar-health-score.yaml
│   ├── mapear-jornada.yaml
│   ├── criar-playbook-onboarding.yaml
│   ├── criar-checklist-ativacao.yaml
│   ├── criar-sequencia-boas-vindas.yaml
│   ├── criar-plano-retencao.yaml
│   ├── criar-qbr.yaml
│   └── criar-plano-risco.yaml
└── workflows/                 # Fluxos de trabalho
    ├── cs-completo.yaml
    └── modo-iniciante-cs.yaml
```

---

## Agentes a Criar

### 1. CSM Estrategista (/csm-estrategia)
Especialista em estrategia de Customer Success responsavel por:
- Definicao de estrategia CS
- Criacao de Health Score
- Segmentacao de base de clientes
- Planejamento de jornadas
- Analise de churn e metricas

Referencias: Lincoln Murphy, Nick Mehta, Gainsight

### 2. Especialista em Onboarding (/onboarding)
Expert em ativacao e primeiro valor responsavel por:
- Design de experiencia de onboarding
- Time to First Value (TTFV)
- Playbooks de ativacao
- Marcos de sucesso iniciais
- Sequencias de comunicacao inicial

Referencias: Wes Bush (Product-Led Onboarding), Intercom

### 3. Especialista em Retencao (/retencao)
Expert em manter e expandir clientes responsavel por:
- Estrategias anti-churn
- Identificacao de clientes em risco
- Processos de reativacao
- Expansion revenue (upsell/cross-sell)
- NPS e pesquisas de satisfacao

Referencias: ChurnZero, Totango, Lincoln Murphy

---

## Tarefas a Criar

### Fase Diagnostico
1. **analise-base-clientes** - Segmentar e diagnosticar base atual
2. **criar-health-score** - Definir metricas de saude do cliente
3. **mapear-jornada** - Mapear jornada atual do cliente

### Fase Onboarding
4. **criar-playbook-onboarding** - Playbook completo de onboarding
5. **criar-checklist-ativacao** - Marcos de ativacao inicial
6. **criar-sequencia-boas-vindas** - Comunicacao de boas-vindas

### Fase Retencao
7. **criar-plano-retencao** - Estrategia anti-churn
8. **criar-qbr** - Business Review estruturado
9. **criar-plano-risco** - Acao para clientes em risco

---

## Workflows a Criar

### 1. CS Completo (/cs-completo)
Processo profissional em 6 fases:

1. **DIAGNOSTICO** - Analise da situacao atual
   - Segmentacao de clientes
   - Mapeamento de jornada
   - Identificacao de gaps

2. **ESTRATEGIA** - Definicao de estrategia CS
   - Health Score
   - Objetivos e metas
   - Playbooks base

3. **ONBOARDING** - Estruturar ativacao
   - Playbook de onboarding
   - Marcos de sucesso
   - Comunicacao inicial

4. **ACOMPANHAMENTO** - Processos ongoing
   - Touchpoints regulares
   - QBRs estruturados
   - Automacoes

5. **RETENCAO** - Prevenir churn
   - Alertas de risco
   - Planos de recuperacao
   - Estrategias proativas

6. **EXPANSION** - Crescer receita
   - Upsell/Cross-sell
   - Advocacy
   - Referencias

### 2. Modo Iniciante (/iniciante-cs)
5 perguntas essenciais:
1. Qual seu produto/servico?
2. Quantos clientes ativos voce tem?
3. Qual seu principal desafio com clientes? (churn, onboarding, etc)
4. Como voce mede sucesso do cliente hoje?
5. Qual resultado mais urgente precisa?

---

## Base de Conhecimento

### Fundamentos (fundamentos-cs.md)
- O que e Customer Success
- Diferenca entre CS, Suporte e Atendimento
- Piramide de valor CS
- Principios de Lincoln Murphy

### Metricas (metricas-cs.md)
- Health Score - como construir
- NPS - Net Promoter Score
- CSAT - Customer Satisfaction
- CES - Customer Effort Score
- Churn Rate e MRR Churn
- Expansion Revenue

### Jornada do Cliente (jornada-cliente.md)
- Fases da jornada
- Touchpoints criticos
- Momentos da verdade
- Mapeamento de jornada

### Onboarding Framework (onboarding-framework.md)
- Time to First Value
- Onboarding tech-touch vs high-touch
- Playbooks de ativacao
- Kickoff meetings
- Marcos de sucesso

### Retencao (retencao-estrategias.md)
- Sinais de churn
- Estrategias de prevencao
- Reativacao de clientes
- Proactive vs Reactive CS

### QBR Playbook (qbr-playbook.md)
- Estrutura de QBR
- Preparacao e agenda
- Metricas a apresentar
- Proximos passos

---

## Referencias e Mestres

### Mestres de Customer Success
- **Lincoln Murphy** - Sixteen Ventures, Customer Success evangelist
- **Nick Mehta** - CEO Gainsight, autor "Customer Success"
- **Dan Steinman** - CCO Gainsight, co-autor "Customer Success"
- **Jason Lemkin** - SaaStr, especialista em SaaS CS

### Frameworks
- **DEAR Framework** (Gainsight) - Deployment, Engagement, Adoption, ROI
- **LAER Model** - Land, Adopt, Expand, Renew
- **Time to First Value** - Metodologia de onboarding
- **Health Score** - Modelo de saude do cliente

### Plataformas de Referencia
- Gainsight
- ChurnZero
- Totango
- ClientSuccess
- Intercom

---

## Instrucoes de Execucao

### Fase 1: Estrutura Base
1. Criar diretorio `extensoes/customer-success/`
2. Criar subdiretorios: agentes/, conhecimento/, tarefas/, workflows/
3. Criar `extensao.yaml` baseado no modelo de marketing
4. Criar `README.md` com documentacao completa

### Fase 2: Agentes
1. Criar CSM-ESTRATEGISTA.md com identidade completa
2. Criar ONBOARDING-SPECIALIST.md com especialidades
3. Criar RETENTION-EXPERT.md com frameworks de retencao
4. Cada agente deve ter: Identidade, Especialidades, Regras, Processo, Referencias

### Fase 3: Conhecimento
1. Criar 6 arquivos de conhecimento
2. Incluir frameworks, metodologias e exemplos
3. Referenciar mestres e plataformas
4. Adicionar templates praticos

### Fase 4: Tarefas
1. Criar 9 tarefas cobrindo diagnostico, onboarding e retencao
2. Cada tarefa: entradas, processo, template de saida, gates
3. Vincular cada tarefa ao agente correto

### Fase 5: Workflows
1. Criar cs-completo.yaml com 6 fases
2. Criar modo-iniciante-cs.yaml com 5 perguntas
3. Incluir checkpoints e entregaveis

### Fase 6: Integracao
1. Atualizar `core/orquestrador/delegacao.yaml`
2. Atualizar `.claude/CLAUDE.md`
3. Registrar comandos e gatilhos

---

## Validacao Final

Antes de concluir, verificar:

- [ ] extensao.yaml valido e completo
- [ ] README.md documenta toda a extensao
- [ ] 3 agentes com identidades claras e referencias
- [ ] 6 arquivos de conhecimento com exemplos
- [ ] 9 tarefas funcionais com templates
- [ ] Workflow completo com 6 fases
- [ ] Modo iniciante com 5 perguntas
- [ ] delegacao.yaml atualizado
- [ ] CLAUDE.md atualizado

---

## Resultado Esperado

Extensao **Customer Success** completamente funcional, permitindo que usuarios:

- Analisem e segmentem sua base de clientes
- Criem Health Score personalizado
- Estruturem onboarding eficiente
- Implementem estrategias de retencao
- Conduzam QBRs profissionais
- Previnam churn proativamente
- Expandam receita com clientes existentes

Seguindo os padroes do Sleep Agent e pronta para uso imediato.
