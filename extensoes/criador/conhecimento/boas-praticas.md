# Boas Práticas - Base de Conhecimento

## Princípios Gerais

### 1. Simplicidade Primeiro
- Começar com o mínimo viável
- Adicionar complexidade gradualmente
- Evitar over-engineering

### 2. Consistência
- Seguir padrões estabelecidos
- Nomenclatura uniforme
- Estruturas previsíveis

### 3. Documentação
- Tudo documentado
- README em cada extensão
- Exemplos práticos

### 4. Modularidade
- Componentes independentes
- Fácil de modificar
- Reutilizável

## Boas Práticas por Componente

### Extensões

#### ✅ Fazer

```yaml
# Escopo bem definido
nome: "Educacional"  # Claro e específico
descricao: "Cursos, aulas e atividades"  # Objetivo

# Componentes mínimos
agentes: [1-5]      # Não exagerar
tarefas: [3-10]     # Cobertura adequada
workflows: [1-3]    # Principais casos de uso

# Integração pensada
integracoes:
  ralph: true       # Se faz sentido
  outras_extensoes:
    - marketing     # Conexões úteis
```

#### ❌ Evitar

```yaml
# Escopo vago
nome: "Coisas"
descricao: "Faz várias coisas"

# Excesso
agentes: [15]       # Muito fragmentado
tarefas: [50]       # Difícil manter

# Isolamento
integracoes: null   # Sem conexões
```

### Agentes

#### ✅ Fazer

```markdown
# Identidade clara
Sou o **Copywriter**, especialista em textos persuasivos.

# Especialidades específicas
- Headlines magnéticas
- Emails de vendas
- Páginas de conversão

# Tom de voz definido
- Direto e persuasivo
- Focado em benefícios
- Linguagem do público

# Regras acionáveis
1. Nunca usar clichês
2. Sempre incluir CTA
3. Benefício > característica
```

#### ❌ Evitar

```markdown
# Vago
Sou um assistente que ajuda com coisas.

# Genérico
- Ajudar pessoas
- Fazer tarefas
- Ser útil

# Tom indefinido
- Às vezes formal
- Às vezes casual

# Regras vagas
1. Ser bom
2. Fazer bem feito
```

### Tarefas

#### ✅ Fazer

```yaml
# Entradas claras
entradas:
  obrigatorias:
    - nome: produto
      pergunta: "O que você está vendendo?"
      tipo: texto
      exemplo: "Curso de confeitaria"

# Passos específicos
passos:
  - numero: 1
    acao: "Analisar público-alvo"
    detalhes:
      - "Identificar dores principais"
      - "Mapear desejos"

# Template de saída completo
saida:
  template: |
    # Headlines

    ## Contexto
    - **Produto:** {{produto}}

    ## Headlines Criadas
    1. {{headline_1}}
```

#### ❌ Evitar

```yaml
# Entradas vagas
entradas:
  - informacoes  # O quê?

# Passos genéricos
passos:
  - "Fazer a tarefa"
  - "Entregar resultado"

# Sem template
saida:
  formato: "qualquer"
```

### Workflows

#### ✅ Fazer

```yaml
# Fases bem definidas
fases:
  - numero: 1
    nome: DESCOBERTA
    agente: estrategista
    tempo_estimado: "30 min"

    etapas:
      - id: briefing
        entregavel: briefing.md

    checkpoint:
      pergunta: "Informações suficientes?"

# Fallbacks planejados
fallbacks:
  se_erro:
    acao: retry
    mensagem: "Vou tentar novamente"

# Entrega clara
entrega_final:
  local: projetos/{{nome}}/
  estrutura: |
    {{nome}}/
    ├── arquivo1.md
    └── arquivo2.md
```

#### ❌ Evitar

```yaml
# Fases vagas
fases:
  - "Fazer coisas"
  - "Terminar"

# Sem fallback
# (usuário fica perdido se erro)

# Entrega indefinida
entrega_final: "em algum lugar"
```

## Checklist de Qualidade

### Nova Extensão

```
PLANEJAMENTO
□ Escopo definido claramente
□ Público-alvo identificado
□ Problema que resolve documentado
□ Resultados esperados listados

ESTRUTURA
□ Diretórios criados corretamente
□ extensao.yaml completo e válido
□ README.md informativo
□ Nomenclatura seguindo padrões

AGENTES
□ Mínimo 1, ideal 3 agentes
□ Cada agente com identidade única
□ Especialidades não sobrepostas
□ Tom de voz definido
□ Regras acionáveis

TAREFAS
□ Tarefas principais identificadas
□ Entradas claras com exemplos
□ Passos documentados
□ Templates de saída completos
□ Gates de qualidade

WORKFLOWS
□ Workflow principal criado
□ Modo iniciante (se aplicável)
□ Fases com checkpoints
□ Entrega final estruturada
□ Integração Ralph (se aplicável)

CONHECIMENTO
□ Base de conhecimento criada
□ Referências documentadas
□ Metodologias explicadas
□ Exemplos incluídos

INTEGRAÇÃO
□ delegacao.yaml atualizado
□ CLAUDE.md atualizado
□ Pastas output criadas
□ Templates Ralph (se aplicável)
□ Testes realizados
```

### Revisão de Agente

```
IDENTIDADE
□ Nome descritivo
□ Propósito claro
□ Missão em uma frase

COMPETÊNCIAS
□ 5-8 especialidades
□ Específicas (não genéricas)
□ Complementares

COMPORTAMENTO
□ Tom de voz definido (3-4 características)
□ Regras acionáveis (5-7)
□ Processo de trabalho documentado

INTEGRAÇÃO
□ Gatilhos mapeados
□ Relação com outros agentes
□ Tarefas vinculadas
```

### Revisão de Tarefa

```
IDENTIFICAÇÃO
□ ID único e descritivo
□ Agente vinculado
□ Comando definido

ENTRADAS
□ Obrigatórias com exemplos
□ Opcionais com defaults
□ Tipos corretos

PROCESSO
□ Passos claros e ordenados
□ Detalhes quando necessário
□ 4-7 passos

SAÍDA
□ Formato especificado
□ Template completo
□ Variáveis mapeadas

QUALIDADE
□ Gates definidos
□ Próximos passos sugeridos
□ Conhecimento referenciado
```

## Anti-Patterns

### 1. Extensão Monolítica
❌ Uma extensão que faz tudo
✅ Extensões focadas por domínio

### 2. Agente Generalista
❌ "Ajuda com qualquer coisa"
✅ Especialidades bem definidas

### 3. Tarefa Vaga
❌ "Criar conteúdo"
✅ "Criar headline usando fórmula AIDA"

### 4. Workflow Sem Fim
❌ Processo infinito sem conclusão
✅ Fases com checkpoints e entrega final

### 5. Documentação Ausente
❌ "O código é auto-explicativo"
✅ README, comentários, exemplos

## Manutenção

### Versionamento
- Usar versionamento semântico (1.0.0)
- Documentar mudanças significativas
- Manter retrocompatibilidade quando possível

### Evolução
- Adicionar features incrementalmente
- Coletar feedback de uso
- Refatorar quando necessário
- Deprecar com aviso prévio

### Testes
- Testar novos componentes
- Validar integrações
- Verificar outputs
- Documentar casos de borda
