# Core do Sleep Agent

O Core é o motor do Sleep Agent, responsável por:

- **Orquestração**: Coordenar agentes e delegar tarefas
- **Templates**: Padronizar formatos de saída
- **Comandos**: Disponibilizar comandos globais

## Estrutura

```
core/
├── orquestrador/
│   ├── ORQUESTRADOR.md    # Prompt e comportamento
│   ├── delegacao.yaml     # Regras de delegação
│   └── qualidade.yaml     # Gates de qualidade
├── templates/
│   ├── tarefa.yaml        # Template de tarefa
│   └── progresso.md       # Template de progresso
└── comandos/
    └── AJUDA.md           # Comando /ajuda
```

## Como Funciona

1. Usuário faz um pedido
2. Orquestrador analisa e identifica intenção
3. Delega para agente especializado
4. Agente executa usando conhecimento da extensão
5. Resultado passa por verificação de qualidade
6. Entrega ao usuário

## Extensibilidade

O Core é independente das extensões. Novas extensões podem ser adicionadas sem modificar o core.
