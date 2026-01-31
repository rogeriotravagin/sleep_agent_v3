# Sleep Agent

Framework de agentes para profissionais que usa o Claude Code como motor.

## O que é

O Sleep Agent transforma o Claude Code em um assistente inteligente com agentes especializados para diferentes áreas profissionais. Sem código, sem instalação complexa - apenas arquivos de configuração que o Claude lê e segue.

## Para quem

Profissionais não-técnicos que querem usar IA de forma produtiva:
- Marketing e copywriting
- Jurídico (em breve)
- Contábil (em breve)

## Início Rápido

```bash
# 1. Clone o repositório
git clone https://github.com/seu-usuario/sleep_agent.git

# 2. Entre na pasta
cd sleep_agent

# 3. Inicie o Claude Code
claude
```

O Claude vai se apresentar como Sleep Agent e mostrar os comandos disponíveis.

## Comandos

### Gerais
| Comando | O que faz |
|---------|-----------|
| `/ajuda` | Menu de ajuda |
| `/extensoes` | Lista extensões |
| `/status` | Status atual |

### Marketing
| Comando | O que faz |
|---------|-----------|
| `/marketing` | Ativa extensão |
| `/copy` | Agente Copywriter |
| `/estrategia` | Agente Estrategista |
| `/ads` | Agente de Tráfego |
| `/criar-oferta` | Criar oferta completa |
| `/criar-headline` | Criar headlines |
| `/criar-email` | Escrever emails |
| `/lancamento` | Workflow de lançamento |

## Estrutura

```
sleep_agent/
├── .claude/CLAUDE.md      # Configuração do Claude
├── core/                  # Motor do sistema
├── extensoes/             # Módulos por área
│   └── marketing/         # Extensão de Marketing
├── projetos/              # Seus projetos
└── docs/                  # Documentação
```

## Como Funciona

1. Você faz um pedido
2. O Sleep Agent identifica qual agente é melhor
3. O agente executa usando conhecimento especializado
4. Você recebe o resultado e pode refinar

## Documentação

- [Instalação](docs/INSTALACAO.md)
- [Primeiros Passos](docs/PRIMEIROS-PASSOS.md)
- [FAQ](docs/FAQ.md)
- [Glossário](docs/GLOSSARIO.md)

## Diferencial

| Aspecto | Outros Frameworks | Sleep Agent |
|---------|-------------------|-------------|
| Arquivos | Centenas | ~30 |
| Instalação | Complexa | git clone |
| Dependências | Várias | Nenhuma |
| Para quem | Desenvolvedores | Profissionais |

## Licença

MIT
