---
name: marketing-campanha
description: Planeja campanhas de marketing integradas — conceito, canais, cronograma, budget e métricas. Use quando o usuário pedir para criar campanha de marketing, planejar ação promocional, estratégia de campanha, plano de comunicação, ou lançamento de produto/serviço com múltiplos canais.
---

# Campanha de Marketing

Planeje campanhas integradas com conceito criativo, distribuição multicanal e métricas.

## Coleta
- Objetivo (awareness, leads, vendas, lançamento)
- Produto/serviço/promoção
- Público-alvo
- Budget disponível
- Período/duração
- Canais disponíveis

## Output

```markdown
# 🚀 Campanha — [Nome da Campanha]
**Período:** [dd/mm — dd/mm]
**Objetivo:** [X]
**Budget:** R$ [X]
**Público:** [X]

## Conceito Criativo
**Big Idea:** [conceito central em 1 frase]
**Mensagem-chave:** [o que o público deve pensar/sentir/fazer]
**Tom:** [X]
**Hashtag:** #[campanha]

## Distribuição por Canal

| Canal | Objetivo | Formato | Budget | KPI |
|-------|----------|---------|--------|-----|
| Meta Ads | [X] | [X] | R$ X | [X] |
| Google Ads | [X] | [X] | R$ X | [X] |
| Instagram orgânico | [X] | [X posts] | — | [X] |
| Email | [X] | [X emails] | — | [X] |
| WhatsApp | [X] | [X msgs] | — | [X] |

## Cronograma

| Fase | Período | Ações | Canais |
|------|---------|-------|--------|
| Teaser | [X dias] | [ações] | [canais] |
| Lançamento | [X dias] | [ações] | [canais] |
| Sustentação | [X dias] | [ações] | [canais] |
| Encerramento | [X dias] | [ações] | [canais] |

## Peças Necessárias
- [ ] [Lista de cada peça criativa necessária]

## Metas e KPIs

| Métrica | Meta | Como Medir |
|---------|------|-----------|
| [alcance/impressões] | [X] | [ferramenta] |
| [leads/conversões] | [X] | [ferramenta] |
| [receita] | R$ [X] | [ferramenta] |
| ROI | [X]x | Receita / Investimento |
```

## Regras
- Toda campanha precisa de um conceito criativo central (não é só desconto)
- Distribua budget por canal baseado em performance histórica
- Cronograma em fases: teaser → lançamento → sustentação → encerramento
- Mensagem consistente mas adaptada ao formato de cada canal
- Defina métricas ANTES de lançar (não depois)
- Campanha sem deadline = campanha infinita = desperdício de budget

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-persona` — use o output como input se já foi rodada
- `/marketing-funil` — use o output como input se já foi rodada

### Passa o bastão para:
- **Campanha precisa de ads** → `/meta-copy-criativo`
- **Campanha precisa de emails** → `/marketing-email`
- **Campanha precisa de conteúdo** → `/instagram-calendario`
- **Resultados → relatório** → `/meta-relatorio-performance`

### Contexto compartilhado
Campanha integrada = mesma mensagem em todos os canais. Garantir consistência.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
