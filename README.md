# Sleep Agent

Framework de agentes para profissionais que usa o Claude Code como motor.

## O que e

O Sleep Agent transforma o Claude Code em um assistente inteligente com agentes especializados para diferentes areas profissionais. Sem codigo, sem instalacao complexa - apenas arquivos de configuracao que o Claude le e segue.

**Arquitetura modular:** Funciona como um sistema de plugins. O core e generico e as extensoes sao independentes.

## Para quem

Profissionais nao-tecnicos que querem usar IA de forma produtiva.

## Inicio Rapido

```bash
# 1. Clone o repositorio
git clone https://github.com/seu-usuario/sleep_agent.git

# 2. Entre na pasta
cd sleep_agent

# 3. Inicie o Claude Code
claude
```

O Claude vai se apresentar como Sleep Agent, configurar seu workspace e mostrar os comandos disponiveis.

## Comandos Globais

| Comando | O que faz |
|---------|-----------|
| `/ajuda` | Menu de ajuda |
| `/setup` | Configurar workspace |
| `/extensoes` | Lista extensoes instaladas |
| `/status` | Status atual |
| `/ralph` | Modo autonomo |

## Estrutura do Projeto

```
sleep_agent/
├── .claude/CLAUDE.md           # Configuracao do Claude (generico)
├── core/                       # Motor central (generico)
│   ├── setup/                  # Agente de configuracao
│   ├── orquestrador/           # Sistema de delegacao
│   └── comandos/               # Comandos globais
├── frameworks/
│   └── ralph/                  # Motor autonomo
├── extensoes/                  # Extensoes instaladas (plugins)
│   └── [extensao]/             # Cada extensao e autocontida
│       ├── .claude/            # Instrucoes especificas
│       ├── core/               # Orquestrador da extensao
│       ├── agentes/            # Agentes especializados
│       ├── conhecimento/       # Base de conhecimento
│       ├── tarefas/            # Definicoes de tarefas
│       └── workflows/          # Fluxos de trabalho
├── workspace/                  # Area de trabalho do usuario
│   └── .config/                # Configuracoes salvas
└── docs/                       # Documentacao
```

## Como Funciona

1. **Setup inicial:** O sistema configura seu workspace (empresa/produto)
2. **Voce faz um pedido:** Descreve o que precisa
3. **Identificacao:** O Sleep Agent identifica qual extensao e agente usar
4. **Execucao:** O agente executa usando conhecimento especializado
5. **Resultado:** Voce recebe o output organizado no workspace

## Sistema de Extensoes

Extensoes sao plugins independentes que adicionam capacidades ao Sleep Agent.

Cada extensao inclui:
- Agentes especializados
- Tarefas e workflows
- Base de conhecimento
- Regras de delegacao proprias

Para adicionar uma extensao, basta colocar a pasta em `extensoes/`.

## Workspace Adaptativo

O workspace se adapta ao seu contexto:

| Cenario | Estrutura |
|---------|-----------|
| Multiplas empresas | workspace/holding/empresa-a/... |
| Uma empresa | workspace/empresa/produtos/... |
| Um produto | workspace/produto/... |

O sistema detecta automaticamente quando voce cresce e reorganiza.

## Documentacao

- [Instalacao](docs/INSTALACAO.md)
- [Primeiros Passos](docs/PRIMEIROS-PASSOS.md)
- [FAQ](docs/FAQ.md)
- [Glossario](docs/GLOSSARIO.md)

## Diferencial

| Aspecto | Outros Frameworks | Sleep Agent |
|---------|-------------------|-------------|
| Arquitetura | Monolitica | Modular (plugins) |
| Instalacao | Complexa | git clone |
| Dependencias | Varias | Nenhuma |
| Para quem | Desenvolvedores | Profissionais |
| Extensivel | Dificil | Adicionar pasta |

## Licenca

MIT
