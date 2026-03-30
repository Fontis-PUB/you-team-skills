---
name: negocios-forecasting
description: Cria projeções financeiras e forecasts de receita, crescimento e cenários. Use quando o usuário pedir projeção financeira, forecast de receita, cenários de crescimento, modelagem financeira, ou planejamento financeiro de negócio.
---

# Forecasting de Negócio

Crie projeções financeiras realistas com cenários e premissas claras.

## Tipos de Forecast

### Revenue Forecast
- Projeção de receita mensal/anual
- Baseada em: pipeline atual, taxa de conversão histórica, sazonalidade

### Growth Model
- Projeção de crescimento por canal
- Modelagem de CAC, LTV, payback
- Curva de adoção (S-curve)

### P&L Projetado
- Receita - Custos - Despesas = Resultado
- Ponto de equilíbrio (break-even)
- Margem de contribuição projetada

## Output

```markdown
# 📈 Forecast — [Empresa] — [Período]

## Premissas

| Premissa | Valor | Base |
|----------|-------|------|
| Crescimento mensal de leads | X% | Histórico 6 meses |
| Taxa de conversão | X% | Média últimos 3 meses |
| Ticket médio | R$ X | Média ponderada |
| Churn mensal | X% | Histórico |
| CAC | R$ X | Últimos 3 meses |

## Cenário Base (mais provável)

| Mês | Leads | Novos Clientes | Receita Nova | Churn | MRR Total |
|-----|-------|----------------|-------------|-------|-----------|
| M1 | X | X | R$ X | R$ X | R$ X |
| M2 | X | X | R$ X | R$ X | R$ X |
| ... | | | | | |
| M12 | X | X | R$ X | R$ X | R$ X |

**Receita anual projetada:** R$ [X]
**Crescimento:** [X]%

## Cenário Otimista (+30% nas premissas de crescimento)
[Tabela resumida]
**Receita anual:** R$ [X]

## Cenário Pessimista (-30% nas premissas)
[Tabela resumida]
**Receita anual:** R$ [X]

## P&L Projetado (Cenário Base)

| Item | Mensal (M6) | Mensal (M12) | Anual |
|------|------------|-------------|-------|
| Receita | R$ X | R$ X | R$ X |
| (-) Custos Variáveis | R$ X | R$ X | R$ X |
| = Margem Bruta | R$ X | R$ X | R$ X |
| (-) Despesas Fixas | R$ X | R$ X | R$ X |
| (-) Marketing | R$ X | R$ X | R$ X |
| (-) Equipe | R$ X | R$ X | R$ X |
| = Resultado | R$ X | R$ X | R$ X |
| Margem | X% | X% | X% |

## Break-Even
- **Data projetada:** Mês [X]
- **MRR necessário:** R$ [X]
- **Clientes necessários:** [X]

## Riscos e Sensibilidade
| Se [premissa] mudar | Impacto na receita |
|---------------------|-------------------|
| Churn +1% | -R$ X/ano |
| CAC +20% | -R$ X/ano |
| Ticket -10% | -R$ X/ano |
```

## Regras
- Sempre declare premissas — forecast sem premissa é chute
- 3 cenários obrigatórios (base, otimista, pessimista)
- Base em dados históricos quando disponíveis (não em esperança)
- Para startups sem histórico: use benchmarks do setor + premissas conservadoras
- Inclua análise de sensibilidade (o que acontece se X mudar Y%)
- Revise forecast mensalmente com dados reais (forecast ≠ set and forget)
- Para SaaS: forecast por cohort é mais preciso que forecast linear

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-kpis` — use o output como input se já foi rodada
- `/whatsapp-crm` — use o output como input se já foi rodada
- `/ops-financeiro` — use o output como input se já foi rodada

### Passa o bastão para:
- **Forecast → pitch** → `/negocios-pitch`
- **Forecast → budget de marketing** → `/marketing-campanha`

### Contexto compartilhado
Premissas vêm dos KPIs reais e do pipeline do CRM. Não chute — use dados.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
