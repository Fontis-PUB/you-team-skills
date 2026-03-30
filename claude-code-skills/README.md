# 56 Skills Claude Code — Seu Time Completo de Negócio

> 56 especialistas que trabalham juntos, passam contexto entre si e nunca perdem informação. Instale no Claude Code e tenha um time inteiro operando em minutos.

```
56 profissionais  ·  8 áreas  ·  6.256 linhas de instrução  ·  17+ frameworks  ·  6 cadeias de handoff
```

---

## O que é isso

Um repositório open source com 56 skills para o Claude Code. Cada skill é um especialista com instruções detalhadas, frameworks reais, benchmarks do mercado brasileiro e templates de output prontos.

O diferencial: elas não são ferramentas isoladas. São um **time integrado** — quando uma skill identifica um problema fora da sua área, ela faz handoff automático para a skill certa, com todo o contexto necessário. O output de uma é o input da próxima.

---

## Instalação

### Pré-requisito

Ter o [Claude Code](https://docs.anthropic.com/en/docs/claude-code) instalado.

### Instalar todas as skills

```bash
# 1. Clone o repositório
git clone https://github.com/fontiss/claude-code-skills.git

# 2. Copie todas as skills para o diretório do Claude Code
cp -r claude-code-skills/01-gestao-trafego/* ~/.claude/skills/
cp -r claude-code-skills/02-estrategista-lancamento/* ~/.claude/skills/
cp -r claude-code-skills/03-social-media-conteudo/* ~/.claude/skills/
cp -r claude-code-skills/04-gestor-comercial/* ~/.claude/skills/
cp -r claude-code-skills/05-marketing-crescimento/* ~/.claude/skills/
cp -r claude-code-skills/06-estrategista-negocios/* ~/.claude/skills/
cp -r claude-code-skills/07-design-identidade/* ~/.claude/skills/
cp -r claude-code-skills/08-operacoes-produto/* ~/.claude/skills/

# 3. Copie o orquestrador do time
cp claude-code-skills/TEAM.md ~/.claude/skills/
```

### Instalar uma skill específica

```bash
# Exemplo: instalar apenas o analista de campanhas Meta
cp -r claude-code-skills/01-gestao-trafego/meta-analise-campanha ~/.claude/skills/
```

### Estrutura de cada skill

```
nome-da-skill/
└── SKILL.md
```

Cada `SKILL.md` contém:
- **Frontmatter YAML** — `name` + `description` (o Claude Code usa isso para acionar a skill automaticamente)
- **Instruções** — framework, coleta de dados, output estruturado, regras de negócio
- **Integração com o Time** — de quem recebe contexto, para quem passa o bastão, protocolo de handoff

---

## Como usar

### Modo 1: Descrever o que precisa (mais natural)

Abra o Claude Code e diga o que quer. A skill é acionada automaticamente pelo `description` no frontmatter.

```
"Analisa essa campanha de Meta Ads, gastei R$5K e quero saber se tá bom"
→ Aciona: meta-analise-campanha

"Monta um cronograma pro meu lançamento, carrinho abre dia 15/05"
→ Aciona: lancamento-cronograma

"Cria 3 variações de legenda pra esse post de carrossel"
→ Aciona: instagram-copy

"Me ajuda a montar uma proposta comercial pra esse cliente"
→ Aciona: comercial-proposta
```

### Modo 2: Rodar o comando direto

```
/meta-analise-campanha
/lancamento-cronograma
/whatsapp-atendimento
/negocios-diagnostico
```

### Modo 3: Rodar o time completo

```
"Faz um diagnóstico completo do meu negócio e monta um plano de ação"
→ Aciona: TEAM.md (orquestrador) → negocios-diagnostico → skills por área conforme score
```

### O que acontece quando você roda uma skill

1. **A skill coleta os dados** — pergunta o que falta (ou usa o que você já forneceu)
2. **Analisa com frameworks e benchmarks** — compara seus números com referências do mercado BR
3. **Entrega output estruturado** — tabelas, semáforos 🟢🟡🔴, checklists, planos de ação
4. **Faz handoff se necessário** — se identificou um problema que outra skill resolve, passa o bastão com contexto

### Exemplo real de handoff

Você roda `/meta-analise-campanha`. O diagnóstico encontra:

```
CPM: R$58 (benchmark R$25) → 🔴 CRÍTICO
CTR: 0.4% (benchmark >1%) → 🔴 CRÍTICO  
Frequência: 6.2 (ideal 1.5-3.0) → 🔴 CRIATIVO QUEIMADO

🔄 Próximo Passo do Time
Handoff para: /meta-copy-criativo
Contexto: CTR abaixo de 1% indica hook fraco. Frequência 6.2 confirma fadiga de criativo.
Dados para passar: público-alvo, produto, tom de voz
Prioridade: 🔴 Urgente
```

Você roda `/meta-copy-criativo`. Ela já sabe que o problema é o hook, usa a persona (se já foi rodada), e entrega 3 variações de copy. Depois sugere handoff para `/meta-audiencia` se os públicos também precisarem de ajuste.

---

## O Organograma do Time

### 01. Gestão de Tráfego — 7 profissionais

| Skill | Função | O que entrega |
|-------|--------|---------------|
| `meta-analise-campanha` | Analista de Campanhas Meta | Diagnóstico com semáforo, benchmarks BR, plano de ação 72h |
| `meta-relatorio-performance` | Relatório de Performance Meta | Report profissional para clientes com comparativos |
| `meta-copy-criativo` | Copywriter de Criativos Meta | 3+ variações com frameworks AIDA/PAS/BAB/4U |
| `meta-audiencia` | Estrategista de Audiências Meta | Mapa de públicos por funil com LAL e exclusões |
| `google-analise-campanha` | Analista de Campanhas Google | Diagnóstico Search/Display/YouTube/PMax |
| `google-relatorio` | Relatório de Performance Google | Report com Quality Score e termos de pesquisa |
| `google-copy` | Copywriter de Anúncios Google | RSAs com contagem de caracteres + extensões |

### 02. Estrategista de Lançamento — 8 profissionais

| Skill | Função | O que entrega |
|-------|--------|---------------|
| `lancamento-cronograma` | Gerente de Cronograma | Timeline por modelo (PLF/Webinário/Desafio/Meteórico) |
| `lancamento-copy` | Copywriter de Lançamento | Copies para todas as fases (captura, CPL, carrinho, VSL) |
| `lancamento-emails-cpl` | Especialista em Emails de CPL | Sequência completa: convite, lembrete, replay |
| `lancamento-emails-carrinho` | Especialista em Emails de Carrinho | 12 emails em 7 dias com gatilhos por dia |
| `lancamento-metricas` | Analista de Métricas | Dashboard de performance + debrief |
| `lancamento-oferta` | Arquiteto de Oferta | Stack de valor, ancoragem, bônus, garantia |
| `lancamento-pagina` | Construtor de Páginas | Estrutura de LP de captura e página de vendas |
| `lancamento-pos-venda` | Gestor de Pós-Venda | Onboarding, pesquisa NPS, reativação |

### 03. Social Media & Conteúdo — 7 profissionais

| Skill | Função | O que entrega |
|-------|--------|---------------|
| `instagram-copy` | Copywriter de Instagram | Legendas com 3 variações e 6 tipos de hook |
| `instagram-calendario` | Planejador Editorial | Mês inteiro com framework AEAC |
| `instagram-roteiro` | Roteirista de Reels | Roteiros com estrutura HDPM (Hook/Dev/PlotTwist/Moral) |
| `instagram-hashtag` | Estrategista de Hashtags | Mix de volume (alta/média/nicho) com sets alternados |
| `conteudo-pauta-seo` | Planejador de Pautas SEO | Keyword research, intenção de busca, outline completo |
| `conteudo-blog` | Redator de Blog | Artigos completos otimizados para SEO |
| `conteudo-script-video` | Roteirista de Vídeo | Scripts para YouTube, VSL e webinários |

### 04. Gestor Comercial — 7 profissionais

| Skill | Função | O que entrega |
|-------|--------|---------------|
| `whatsapp-atendimento` | Closer de WhatsApp | Script em 5 etapas + templates de objeção |
| `whatsapp-disparos` | Especialista em Disparos | Campanhas segmentadas com cronograma |
| `whatsapp-chatbot` | Arquiteto de Chatbot | Fluxos com árvore de decisão e handoff humano |
| `whatsapp-crm` | Gestor de CRM WhatsApp | Pipeline com etiquetas, métricas e rotina diária |
| `comercial-proposta` | Redator de Propostas | Proposta profissional com 3 planos e ancoragem |
| `comercial-crm` | Gestor de Pipeline | Estrutura de CRM com campos, etapas e automações |
| `comercial-follow-up` | Especialista em Follow-up | Cadência de 7 touchpoints em 21 dias |

### 05. Marketing & Crescimento — 7 profissionais

| Skill | Função | O que entrega |
|-------|--------|---------------|
| `marketing-funil` | Estrategista de Funil | Funil completo com calculadora reversa |
| `marketing-email` | Especialista em Email Marketing | Sequências (welcome, nutrição, reengajamento, abandono) |
| `marketing-persona` | Pesquisador de Persona/ICP | Perfil completo com dores, desejos e frases reais |
| `marketing-concorrentes` | Analista de Concorrência | Mapeamento competitivo com oportunidades |
| `marketing-seo` | Estrategista de SEO | Auditoria + roadmap 6 meses + topic clusters |
| `marketing-campanha` | Planejador de Campanhas | Campanha integrada multicanal com cronograma |
| `influencer` | Gestor de Influenciadores | Seleção, briefing, contrato e métricas |

### 06. Estrategista de Negócios — 7 profissionais

| Skill | Função | O que entrega |
|-------|--------|---------------|
| `negocios-diagnostico` | Consultor de Diagnóstico | Health score A-F por área + SWOT + plano 90 dias |
| `negocios-precificacao` | Especialista em Precificação | Análise custo/valor/competitivo com 3 planos |
| `negocios-proposta` | Redator de Propostas de Consultoria | Proposta com diagnóstico, metodologia e fases |
| `negocios-processos` | Documentador de Processos | SOPs, fluxos e playbooks operacionais |
| `negocios-kpis` | Definidor de KPIs | Dashboard por modelo de negócio + rotina de review |
| `negocios-forecasting` | Analista de Forecast | Projeções com 3 cenários + análise de sensibilidade |
| `negocios-pitch` | Construtor de Pitch Deck | Deck para investidores/clientes (10-12 slides) |

### 07. Design & Identidade — 6 profissionais

| Skill | Função | O que entrega |
|-------|--------|---------------|
| `design-briefing` | Redator de Briefings | Briefing completo com moodboard, specs e DON'Ts |
| `design-brand` | Documentador de Marca | Brand book com logo, cores, tipografia, tom de voz |
| `design-prompts-ia` | Engenheiro de Prompts Visuais | Prompts para Midjourney/DALL-E/SD com parâmetros |
| `design-ui-ux` | Especificador de UI/UX | Wireframes textuais, user flows, design system |
| `design-apresentacao` | Estruturador de Apresentações | Deck slide a slide com notas de apresentador |
| `design-naming` | Especialista em Naming | 5+ opções com avaliação, domínio e INPI |

### 08. Operações & Produto — 7 profissionais

| Skill | Função | O que entrega |
|-------|--------|---------------|
| `ops-rh` | Gestor de RH | Job descriptions, onboarding 30-60-90, avaliação, PDI |
| `ops-cs` | Gestor de Customer Success | Health score, playbooks por estágio, NPS |
| `ops-documentacao` | Documentador | Wikis, knowledge bases, templates padronizados |
| `ops-financeiro` | Controller Financeiro | DRE gerencial, fluxo de caixa, budget, unit economics |
| `ops-produto` | Product Manager | Roadmap, PRDs, user stories, priorização RICE |
| `ops-automacao` | Arquiteto de Automações | Fluxos Make/Zapier/n8n com tratamento de erro e ROI |
| `ops-dados` | Analista de Dados | Análise cohort, funil, Pareto, RFM |

### Orquestrador — TEAM.md

O "CEO" do time. Sabe quem faz o quê, quem passa o bastão pra quem, e monta planos integrados.

---

## Como o time trabalha junto

As skills não operam isoladas. Estão organizadas em **6 cadeias de trabalho**:

### Cadeia de Tráfego
```
meta-analise-campanha
  → [CTR baixo?] → meta-copy-criativo
  → [CPM alto?] → meta-audiencia
  → [CPA alto + CTR bom?] → lancamento-pagina
  → [resultados prontos] → meta-relatorio-performance
  → [investimento] → ops-financeiro
```

### Cadeia de Lançamento
```
marketing-persona → lancamento-oferta → lancamento-pagina → lancamento-copy
  → lancamento-cronograma → lancamento-emails-cpl → lancamento-emails-carrinho
  → meta-audiencia → meta-copy-criativo → lancamento-metricas → lancamento-pos-venda
```

### Cadeia Comercial
```
marketing-funil → whatsapp-chatbot → whatsapp-atendimento → comercial-proposta
  → comercial-follow-up → comercial-crm → whatsapp-crm → ops-cs
```

### Cadeia de Conteúdo
```
marketing-persona → marketing-concorrentes → conteudo-pauta-seo
  → instagram-calendario → instagram-copy → instagram-roteiro
  → instagram-hashtag → conteudo-blog → conteudo-script-video
```

### Cadeia Estratégica
```
negocios-diagnostico → negocios-kpis → negocios-precificacao
  → negocios-forecasting → negocios-pitch → negocios-processos
```

### Cadeia de Operações
```
negocios-diagnostico → ops-produto → ops-rh → ops-documentacao
  → ops-automacao → ops-financeiro → ops-dados → ops-cs
```

---

## Workflows prontos

Cenários completos que acionam múltiplas skills em sequência:

| Cenário | Sequência de Skills |
|---------|-------------------|
| "Quero lançar um produto do zero" | persona → oferta → página → cronograma → copy → emails CPL → emails carrinho → audiência → copy criativo → métricas → pós-venda |
| "Minha empresa tá travada" | diagnóstico → KPIs → funil → financeiro → processos → automação |
| "Quero começar no digital" | persona → concorrentes → precificação → funil → calendário → pauta SEO → WhatsApp atendimento |
| "Quero escalar meu tráfego" | meta-análise → audiência → copy criativo → relatório → financeiro |
| "Quero montar meu time comercial" | CRM → WhatsApp atendimento → chatbot → proposta → follow-up → CS |
| "Preciso melhorar minha presença digital" | persona → concorrentes → calendário → roteiro → hashtag → pauta SEO → blog |

---

## O que tem dentro de cada skill

Cada SKILL.md contém:

**Frameworks reais** — AIDA, PAS, BAB, 4U para copy. BANT para qualificação. RICE para produto. HDPM para roteiros. AEAC para calendário editorial. PASTOR para página de vendas.

**Benchmarks do mercado brasileiro** — CPM R$15-40 para Meta Ads. CTR acima de 1% para feed. CPA abaixo de 30% do ticket. Conversão de lista 1-3%. Presença em CPL acima de 30%.

**Templates de output** — Tabelas com semáforo 🟢🟡🔴, checklists, diagnósticos com priorização, cronogramas dia a dia. Formato markdown padronizado.

**Regras de ouro** — "Frequência acima de 5 = rode criativo antes de qualquer coisa." "Lead sem resposta em 24h = lead morto." "Onboarding em 48h reduz reembolso em 50%."

**Integração com o time** — Cada skill sabe de quem recebe contexto, para quem passa o bastão, e o protocolo de handoff.

---

## Perguntas frequentes

**Preciso saber programar?**
Não. Instala, descreve o que precisa, e a skill entrega o resultado.

**Funciona no Claude Code gratuito?**
Sim. As skills são arquivos `.md` que o Claude Code lê automaticamente.

**Posso editar as skills?**
Sim. É open source. Edita, melhora, adiciona as suas, faz fork.

**Quanto custa?**
R$0. Pra sempre. Sem login, sem prazo, sem plataforma de terceiro.

**Como atualizo?**
```bash
cd claude-code-skills && git pull
```

---

## Estrutura do repositório

```
claude-code-skills/
├── README.md
├── TEAM.md                              ← Orquestrador do time
├── 01-gestao-trafego/
│   ├── meta-analise-campanha/SKILL.md
│   ├── meta-relatorio-performance/SKILL.md
│   ├── meta-copy-criativo/SKILL.md
│   ├── meta-audiencia/SKILL.md
│   ├── google-analise-campanha/SKILL.md
│   ├── google-relatorio/SKILL.md
│   └── google-copy/SKILL.md
├── 02-estrategista-lancamento/
│   ├── lancamento-cronograma/SKILL.md
│   ├── lancamento-copy/SKILL.md
│   ├── lancamento-emails-cpl/SKILL.md
│   ├── lancamento-emails-carrinho/SKILL.md
│   ├── lancamento-metricas/SKILL.md
│   ├── lancamento-oferta/SKILL.md
│   ├── lancamento-pagina/SKILL.md
│   └── lancamento-pos-venda/SKILL.md
├── 03-social-media-conteudo/
│   ├── instagram-copy/SKILL.md
│   ├── instagram-calendario/SKILL.md
│   ├── instagram-roteiro/SKILL.md
│   ├── instagram-hashtag/SKILL.md
│   ├── conteudo-pauta-seo/SKILL.md
│   ├── conteudo-blog/SKILL.md
│   └── conteudo-script-video/SKILL.md
├── 04-gestor-comercial/
│   ├── whatsapp-atendimento/SKILL.md
│   ├── whatsapp-disparos/SKILL.md
│   ├── whatsapp-chatbot/SKILL.md
│   ├── whatsapp-crm/SKILL.md
│   ├── comercial-proposta/SKILL.md
│   ├── comercial-crm/SKILL.md
│   └── comercial-follow-up/SKILL.md
├── 05-marketing-crescimento/
│   ├── marketing-funil/SKILL.md
│   ├── marketing-email/SKILL.md
│   ├── marketing-persona/SKILL.md
│   ├── marketing-concorrentes/SKILL.md
│   ├── marketing-seo/SKILL.md
│   ├── marketing-campanha/SKILL.md
│   └── influencer/SKILL.md
├── 06-estrategista-negocios/
│   ├── negocios-diagnostico/SKILL.md
│   ├── negocios-precificacao/SKILL.md
│   ├── negocios-proposta/SKILL.md
│   ├── negocios-processos/SKILL.md
│   ├── negocios-kpis/SKILL.md
│   ├── negocios-forecasting/SKILL.md
│   └── negocios-pitch/SKILL.md
├── 07-design-identidade/
│   ├── design-briefing/SKILL.md
│   ├── design-brand/SKILL.md
│   ├── design-prompts-ia/SKILL.md
│   ├── design-ui-ux/SKILL.md
│   ├── design-apresentacao/SKILL.md
│   └── design-naming/SKILL.md
└── 08-operacoes-produto/
    ├── ops-rh/SKILL.md
    ├── ops-cs/SKILL.md
    ├── ops-documentacao/SKILL.md
    ├── ops-financeiro/SKILL.md
    ├── ops-produto/SKILL.md
    ├── ops-automacao/SKILL.md
    └── ops-dados/SKILL.md
```

---

## Licença

MIT — use, modifique, distribua, venda. Crédito é bem-vindo mas não obrigatório.

---

**Criado por [Fontiss](https://github.com/fontiss)** — Construído com Claude.
