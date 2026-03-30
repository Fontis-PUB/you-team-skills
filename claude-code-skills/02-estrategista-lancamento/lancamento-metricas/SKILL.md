---
name: lancamento-metricas
description: Analisa e acompanha métricas de lançamento digital — CPL, taxa de presença, conversão de carrinho, ROI, faturamento vs meta. Use quando o usuário pedir para analisar resultados de lançamento, calcular ROI de lançamento, avaliar métricas de CPL/carrinho, fazer debrief de lançamento, ou acompanhar performance de um lançamento em andamento.
---

# Métricas de Lançamento

Analise a performance de cada fase do lançamento com benchmarks do mercado brasileiro de infoprodutos.

## Métricas por Fase

### PPL (Captação)
- Leads captados — meta vs. real
- CPL (Custo por Lead) — benchmark: R$2-8 (frio), R$0.50-2 (orgânico)
- Taxa de conversão da LP — benchmark: 25-45%
- Custo total de captação

### PL (Evento/CPLs)
- Taxa de presença CPL1 — benchmark: 30-50% da lista
- Retenção entre CPLs — benchmark: 60-80% (CPL1→CPL2), 50-70% (CPL2→CPL3)
- Engajamento (comentários, mensagens) — indicador qualitativo
- Leads aquecidos ao final do PL

### Carrinho
- Taxa de conversão — benchmark: 1-3% da lista total, 5-15% dos que assistiram
- Faturamento total
- Ticket médio real
- Vendas por dia (curva — deve ter pico D1 e D7)
- Recuperação de boletos/PIX — benchmark: 20-40%
- Taxa de reembolso — benchmark: <5% em 7 dias

### Consolidado
- ROI do lançamento = (Faturamento - Custos) / Custos
- CAC (Custo de Aquisição de Cliente) = Investimento total / Clientes
- LTV estimado vs. CAC
- Receita líquida (- impostos, - gateway, - reembolsos, - afiliados)

## Estrutura do Output

```markdown
# 📊 Dashboard de Lançamento — [Produto]
**Período:** [dd/mm — dd/mm]

## Funil Completo

| Etapa | Volume | Taxa | Benchmark | Status |
|-------|--------|------|-----------|--------|
| Impressões tráfego | X | — | — | — |
| Cliques LP | X | CTR X% | >1% | 🟢 |
| Leads captados | X | Conv LP X% | 25-45% | 🟢 |
| Presença CPL1 | X | X% da lista | 30-50% | 🟡 |
| Presença CPL3 | X | X% da lista | 20-35% | 🟢 |
| Vendas | X | X% da lista | 1-3% | 🟢 |

## Financeiro

| Item | Valor |
|------|-------|
| Faturamento Bruto | R$ X |
| (-) Gateway (X%) | R$ X |
| (-) Impostos estimados | R$ X |
| (-) Reembolsos | R$ X |
| (-) Afiliados | R$ X |
| = Receita Líquida | R$ X |
| (-) Investimento tráfego | R$ X |
| (-) Outros custos | R$ X |
| = Lucro Líquido | R$ X |
| ROI | X% |

## Diagnóstico
[Onde estão os gargalos: captação, presença, conversão, ou ticket?]

## Aprendizados para Próximo Lançamento
1. [O que manter]
2. [O que mudar]
3. [O que testar]
```

## Regras
- Se conversão da lista é <1%, o problema está no evento ou na oferta (não no tráfego)
- Se presença CPL1 é <25%, o problema está na captação (promessa fraca ou lead desqualificado)
- Se D1 vende mais que 50% do total, o carrinho está fraco — melhorar sequência de emails
- Se D7 não tem pico, a escassez não está funcionando — verificar comunicação
- Sempre calcule receita LÍQUIDA, nunca apresente apenas faturamento bruto
- Para debrief: compare com lançamento anterior quando disponível

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/lancamento-emails-cpl` — use o output como input se já foi rodada
- `/lancamento-emails-carrinho` — use o output como input se já foi rodada
- `/meta-analise-campanha` — use o output como input se já foi rodada

### Passa o bastão para:
- **Gargalo no tráfego** → `/meta-analise-campanha`
- **Gargalo na conversão** → `/lancamento-pagina`
- **Gargalo na oferta** → `/lancamento-oferta`
- **Debrief completo → preparar próximo** → `/lancamento-cronograma`
- **Receita no DRE** → `/ops-financeiro`

### Contexto compartilhado
Este é o juiz do lançamento. Conecta os dados de todas as fases para identificar onde o funil quebrou.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
