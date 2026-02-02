# Extensao Juridico

Framework completo de suporte juridico empresarial para o Sleep Agent.

## Comando de Ativacao

```
/juridico
```

## O que faz

A extensao Juridico oferece suporte completo para questoes juridicas empresariais:

- **Contratos** - Elaboracao, revisao e analise de contratos comerciais
- **Compliance** - LGPD, politicas internas e programas de conformidade
- **Direito Empresarial** - Societario, M&A, governanca corporativa
- **Trabalhista** - Contratos de trabalho e relacoes trabalhistas

## Agentes Disponiveis

| Agente | Comando | Especialidade |
|--------|---------|---------------|
| Especialista em Contratos | `/contratos` | Elaboracao e revisao de contratos |
| Advogado Empresarial | `/empresarial` | Societario, M&A, governanca |
| Especialista em Compliance | `/compliance` | LGPD, politicas, auditorias |

## Tarefas Rapidas

```
/criar-contrato       - Elaborar contrato personalizado
/revisar-contrato     - Analisar e sugerir alteracoes
/criar-parecer        - Elaborar parecer juridico
/analise-risco        - Mapear riscos juridicos
/politica-privacidade - Criar politica LGPD
/termos-uso           - Criar termos de uso
/nda                  - Acordo de confidencialidade
/contrato-trabalho    - Contratos trabalhistas
```

## Workflows Completos

```
/due-diligence        - Analise completa para aquisicoes
/abertura-empresa     - Estruturacao societaria completa
/programa-compliance  - Implementar programa de compliance
```

## Exemplos de Uso

### Criar um contrato de prestacao de servicos
```
/criar-contrato
Tipo: Prestacao de servicos
Partes: Minha empresa e cliente X
Valor: R$ 5.000/mes
Prazo: 12 meses
```

### Revisar contrato existente
```
/revisar-contrato
[Cola ou anexa o contrato para analise]
```

### Criar politica de privacidade LGPD
```
/politica-privacidade
Site: meusite.com.br
Dados coletados: nome, email, telefone
Finalidade: newsletter e contato comercial
```

## Estrutura de Outputs

Os documentos gerados sao organizados em:

```
workspace/[empresa]/juridico/
├── contratos/
│   ├── prestacao-servicos/
│   ├── parcerias/
│   └── ndas/
├── pareceres/
├── compliance/
│   ├── politicas/
│   └── termos/
└── analises/
```

## Importante

Esta extensao oferece **suporte e orientacao juridica** para auxiliar na criacao de documentos. Os outputs gerados devem ser **revisados por um advogado** antes de uso em situacoes reais que envolvam riscos juridicos significativos.

## Referencias Base

- Codigo Civil Brasileiro
- LGPD (Lei 13.709/2018)
- Marco Civil da Internet
- Lei das S/A
- CLT e Reforma Trabalhista
- Lei Anticorrupcao

## Versao

1.0 - Framework Juridico Empresarial
