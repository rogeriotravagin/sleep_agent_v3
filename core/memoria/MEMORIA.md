# Sistema de Memoria do Sleep Agent

O Sleep Agent possui um sistema de memoria que persiste informacoes importantes entre sessoes, permitindo que o assistente "lembre" de decisoes, padroes e aprendizados anteriores.

---

## Por que usar Memoria?

Imagine que voce contratou um assistente que sempre esquece tudo no dia seguinte. Frustrante, nao? O sistema de memoria resolve isso:

- **Nao precisa repetir** informacoes que ja deu
- **Aprende** com erros e acertos anteriores
- **Mantem consistencia** nas decisoes ao longo do tempo
- **Evolui** junto com seu negocio

---

## Onde fica a Memoria?

A memoria fica na pasta do seu workspace:

```
workspace/.memoria/
├── insights.yaml    # Aprendizados e descobertas
├── decisoes.yaml    # Historico de decisoes importantes
├── padroes.yaml     # Padroes identificados no seu negocio
└── alertas.yaml     # Armadilhas e erros a evitar
```

---

## Tipos de Memoria

### 1. Insights (Aprendizados)

Coisas que o Sleep Agent descobriu trabalhando com voce:

```yaml
# Exemplo de insights.yaml
- data: "2026-02-06"
  categoria: "publico"
  insight: "Seu publico prefere conteudo pratico a teorico"
  contexto: "Descoberto ao criar emails de vendas"

- data: "2026-02-06"
  categoria: "marca"
  insight: "Tom mais informal funciona melhor para sua audiencia"
  contexto: "Teste A/B de headlines"
```

### 2. Decisoes (Historico)

Decisoes importantes que voce tomou:

```yaml
# Exemplo de decisoes.yaml
- data: "2026-02-06"
  decisao: "Usar azul como cor principal da marca"
  motivo: "Transmite confianca e profissionalismo"
  area: "branding"

- data: "2026-02-06"
  decisao: "Preco do produto principal: R$ 497"
  motivo: "Baseado em pesquisa de concorrentes"
  area: "oferta"
```

### 3. Padroes (Consistencia)

Padroes que devem ser seguidos:

```yaml
# Exemplo de padroes.yaml
- area: "comunicacao"
  padrao: "Sempre usar voce (nao tu ou vos)"
  aplicacao: "Todos os textos e emails"

- area: "visual"
  padrao: "Fonte: Montserrat para titulos, Open Sans para corpo"
  aplicacao: "Landing pages e materiais"
```

### 4. Alertas (Evitar Erros)

Armadilhas e erros para nao repetir:

```yaml
# Exemplo de alertas.yaml
- data: "2026-02-06"
  alerta: "Nao usar termos tecnicos com esse publico"
  motivo: "Emails com jargoes tiveram baixa conversao"
  severidade: "alta"

- data: "2026-02-06"
  alerta: "Evitar promessas de resultado garantido"
  motivo: "Pode gerar problemas juridicos"
  severidade: "critica"
```

---

## Como o Sleep Agent usa a Memoria

### Ao Iniciar uma Tarefa

1. **Consulta** a memoria relevante para a tarefa
2. **Aplica** insights e padroes automaticamente
3. **Evita** erros listados nos alertas

### Ao Finalizar uma Tarefa

1. **Captura** novos insights descobertos
2. **Registra** decisoes tomadas
3. **Atualiza** padroes se necessario
4. **Adiciona** alertas se encontrou armadilhas

---

## Comandos de Memoria

| Comando | O que faz |
|---------|-----------|
| `/memoria` | Ver resumo da memoria atual |
| `/memoria insights` | Ver todos os insights |
| `/memoria decisoes` | Ver historico de decisoes |
| `/memoria padroes` | Ver padroes definidos |
| `/memoria alertas` | Ver alertas ativos |
| `/memoria adicionar` | Adicionar item manualmente |
| `/memoria limpar` | Limpar memoria (cuidado!) |

---

## Boas Praticas

### Quando Adicionar Manualmente

- Informacoes importantes sobre seu negocio
- Preferencias pessoais de estilo
- Restricoes que devem ser sempre respeitadas
- Erros que ja cometeu e nao quer repetir

### Quando Deixar o Sleep Agent Adicionar

- Insights descobertos durante o trabalho
- Padroes que emergem naturalmente
- Decisoes tomadas durante tarefas

---

## Privacidade

A memoria fica **apenas no seu computador**, na pasta do workspace. Nada e enviado para servidores externos. Voce tem controle total sobre o que fica armazenado.

---

## Migracao e Backup

### Fazer Backup

Basta copiar a pasta `workspace/.memoria/` para um local seguro.

### Restaurar

Cole a pasta de volta no lugar original.

### Migrar para Novo Workspace

Copie a pasta `.memoria/` do workspace antigo para o novo.
