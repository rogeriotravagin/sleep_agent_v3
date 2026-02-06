# Health Check - Sistema de Saude do Sleep Agent

O Sleep Agent verifica automaticamente sua propria "saude" e corrige problemas comuns sem precisar incomodar voce.

---

## O que e Health Check?

Imagine um assistente que, antes de comecar a trabalhar, verifica se tem tudo que precisa. Se falta algo, ele proprio resolve (quando possivel) ou te avisa de forma clara.

**Beneficios:**
- Menos erros durante o uso
- Problemas corrigidos antes de causar transtorno
- Voce so e acionado quando realmente necessario

---

## 3 Niveis de Problemas

### Nivel 1: Auto-Correcao Silenciosa

Problemas simples que o Sleep Agent resolve sozinho, sem te avisar.

**O que entra aqui:**
- Criar arquivo de configuracao se nao existe
- Criar pastas que faltam no workspace
- Limpar arquivos temporarios antigos
- Corrigir permissoes de arquivos

**Voce nem fica sabendo** - simplesmente funciona.

### Nivel 2: Correcao com Aviso

Problemas que podem ser corrigidos, mas voce deve saber.

**O que entra aqui:**
- Atualizar estrutura do workspace para nova versao
- Migrar configuracoes antigas
- Reparar links quebrados

**O que acontece:**
```
[Aviso] Detectei que sua configuracao esta em formato antigo.
        Posso atualizar para o novo formato automaticamente.
        Suas informacoes serao preservadas.

        Deseja que eu atualize? (sim/nao)
```

### Nivel 3: Intervencao Necessaria

Problemas que so voce pode resolver.

**O que entra aqui:**
- Arquivos importantes corrompidos
- Conflitos que precisam de decisao
- Permissoes de sistema

**O que acontece:**
```
[Atencao] Encontrei um problema que precisa da sua ajuda.

Problema: O arquivo de configuracao esta corrompido.

O que voce pode fazer:
1. Recriar a configuracao do zero (perde personalizacoes)
2. Restaurar de um backup (se tiver)
3. Me mostrar o arquivo para eu tentar diagnosticar

O que prefere?
```

---

## Quando o Health Check Executa

### Automaticamente

1. **Ao iniciar uma sessao** - Verifica se tudo esta ok
2. **Ao carregar uma extensao** - Verifica se extensao esta intacta
3. **Ao salvar arquivo** - Verifica se consegue salvar

### Manualmente

Voce pode pedir:
- `/saude` - Ver status geral do sistema
- `/diagnostico` - Analise detalhada de problemas

---

## O que e Verificado

### Configuracao

| Verificacao | Nivel | Auto-Correcao |
|-------------|-------|---------------|
| sleep-agent.yaml existe | 1 | Criar com valores padrao |
| Formato YAML valido | 3 | Nao (pode perder dados) |
| Versao compativel | 2 | Migrar se possivel |

### Workspace

| Verificacao | Nivel | Auto-Correcao |
|-------------|-------|---------------|
| Pasta .config existe | 1 | Criar pasta |
| Pasta .memoria existe | 1 | Criar pasta |
| Pasta .status existe | 1 | Criar pasta |
| Estrutura de pastas valida | 2 | Sugerir correcao |

### Extensoes

| Verificacao | Nivel | Auto-Correcao |
|-------------|-------|---------------|
| extensao.yaml existe | 3 | Nao (extensao invalida) |
| Formato do manifesto valido | 3 | Nao |
| Agentes referenciados existem | 2 | Alertar quais faltam |
| Conhecimento referenciado existe | 2 | Alertar quais faltam |

### Memoria

| Verificacao | Nivel | Auto-Correcao |
|-------------|-------|---------------|
| Arquivos YAML validos | 2 | Backup + recriar |
| Entradas nao duplicadas | 1 | Remover duplicatas |

---

## Mensagens Amigaveis

O Sleep Agent sempre explica problemas de forma simples:

**Ruim:**
```
Error: ENOENT: no such file or directory, open 'workspace/.config/sleep-agent.yaml'
```

**Bom:**
```
Percebi que e sua primeira vez aqui!
Vou configurar seu espaco de trabalho rapidinho.

[Configurando...] Pronto! Tudo certo para comecar.
```

---

**Ruim:**
```
YAML parse error at line 15: expected ':' but found '-'
```

**Bom:**
```
O arquivo de configuracao tem um pequeno problema de formatacao.

Encontrei o problema na linha 15: falta um ':' depois de 'nome'

Posso corrigir isso automaticamente? (sim/nao)
```

---

## Comandos

| Comando | O que faz |
|---------|-----------|
| `/saude` | Ver status geral do sistema |
| `/diagnostico` | Analise completa e detalhada |
| `/reparar` | Tentar corrigir problemas automaticamente |

---

## Logs de Health Check

Todas as verificacoes e correcoes ficam registradas em:
```
workspace/.status/health-log.yaml
```

Voce pode consultar o historico para entender o que aconteceu:
```yaml
- data: "2026-02-06T10:30:00"
  tipo: "auto-correcao"
  problema: "Pasta .memoria nao existia"
  acao: "Criada pasta .memoria com arquivos padrao"

- data: "2026-02-06T10:31:00"
  tipo: "aviso"
  problema: "Configuracao em formato antigo"
  acao: "Usuario optou por migrar"
  resultado: "Migracao concluida com sucesso"
```

---

## Dicas

1. **Nao se preocupe** - A maioria dos problemas e resolvida automaticamente
2. **Faca backups** - O sistema ajuda, mas backup e sempre bom
3. **Relate problemas** - Se algo parece errado, pergunte
4. **Confie nos avisos** - Se o sistema pede atencao, vale verificar
