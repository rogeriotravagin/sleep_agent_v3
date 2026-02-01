# Ralph Prompt - Design Analyst Agent

## Contexto

Voce esta criando um novo agente para a extensao de Branding do Sleep Agent. O agente "Design Analyst" e especializado em:

1. **Analisar referencias visuais** - Receber prints, links de paginas, ou qualquer referencia visual
2. **Extrair padroes de design** - Identificar e documentar elementos visuais
3. **Criar diretrizes especificas** - Gerar style guides e diretrizes para o produto

## Arquivos de Referencia OBRIGATORIOS

ANTES de criar qualquer arquivo, LEIA os arquivos de referencia:

1. **Para agente:** `extensoes/branding/agentes/DESIGNER.md`
2. **Para tarefa:** `extensoes/branding/tarefas/criar-logo.yaml`
3. **Para workflow:** `extensoes/branding/workflows/brand-completo.yaml`
4. **Para conhecimento:** `extensoes/branding/conhecimento/logo-design.md`
5. **Para extensao.yaml:** `extensoes/branding/extensao.yaml`
6. **Para delegacao.yaml:** `core/orquestrador/delegacao.yaml`

## Instrucoes de Execucao

### Para cada User Story:

1. **Leia o arquivo de referencia** correspondente
2. **Siga o formato exato** - estrutura, secoes, nomenclatura
3. **Crie o arquivo** no local especificado em outputFile
4. **Valide** contra acceptance criteria
5. **Atualize progress.txt** com a sessao

### Especificacoes do Agente Design Analyst

**Especialidades:**
- Analise de referencias visuais (prints, screenshots, links)
- Reverse engineering de design
- Extracao de padroes visuais
- Criacao de style guides
- Documentacao de diretrizes

**Referencias a incluir:**
- Josef Muller-Brockmann (Grid Systems)
- Jan Tschichold (Typography)
- Dieter Rams (10 Principles)
- Ellen Lupton (Thinking with Type)
- Gestalt Principles

**Processo de trabalho:**
1. CAPTURA - Receber e processar referencia
2. DESCONSTRUCAO - Quebrar em elementos
3. ANALISE - Identificar padroes
4. PADROES - Extrair regras
5. SINTESE - Consolidar diretrizes
6. DOCUMENTACAO - Gerar style guide

**Comando:** `/design-analyst`

**Tarefas:**
- `/analisar-referencia` - Analisar uma referencia visual
- `/extrair-diretrizes` - Extrair diretrizes de design
- `/criar-styleguide` - Criar style guide do produto

## Validacao

Cada arquivo deve:
- Estar no local correto
- Seguir o formato dos arquivos de referencia
- Ter conteudo completo e util
- Integrar com o sistema existente

## Output

Todos os arquivos devem ser criados diretamente nos locais especificados em outputFile de cada user story, NAO no diretorio de output.
