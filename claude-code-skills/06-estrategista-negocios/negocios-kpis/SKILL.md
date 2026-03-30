---
name: negocios-kpis
description: Define e estrutura KPIs e dashboards de gestão por área, modelo de negócio e estágio. Use quando o usuário pedir para definir KPIs, métricas de negócio, indicadores de performance, dashboard de gestão, OKRs, ou sistema de acompanhamento de resultados.
---

# KPIs e Métricas de Negócio

Defina indicadores-chave que direcionam decisões por área e modelo de negócio.

## KPIs por Modelo

### SaaS
- **MRR/ARR** — receita recorrente mensal/anual
- **NRR** — Net Revenue Retention (>100% = expansão)
- **Churn Rate** — cancelamento mensal (<2% é bom)
- **CAC** — custo de aquisição
- **LTV** — lifetime value (LTV/CAC > 3x)
- **Payback Period** — meses para recuperar CAC (<12)
- **Activation Rate** — % que completa onboarding

### E-commerce
- **GMV** — volume bruto de vendas
- **AOV** — ticket médio
- **Conversion Rate** — taxa de conversão (>2%)
- **CAC** — custo de aquisição
- **ROAS** — retorno sobre investimento em ads (>3x)
- **Repeat Purchase Rate** — taxa de recompra
- **Abandonment Rate** — taxa de abandono de carrinho

### Serviços/Agência
- **Receita por funcionário**
- **Utilization Rate** — % do tempo faturável (>70%)
- **Ticket médio por projeto**
- **NPS** — satisfação do cliente
- **Churn de clientes**
- **Pipeline/Receita ratio** — cobertura do pipeline

### Infoprodutos
- **Faturamento por lançamento**
- **CPL** — custo por lead
- **Taxa de conversão da lista**
- **ROI do lançamento**
- **Taxa de reembolso** (<5%)
- **NPS dos alunos**

## Output

```markdown
# 📊 Dashboard de KPIs — [Empresa]
**Modelo:** [SaaS/E-com/Serviço/Info]
**Período:** [mês/trimestre]

## Indicadores Principais (North Star + 3-5 KPIs)

**North Star Metric:** [a métrica que mais importa]

| KPI | Atual | Meta | Tendência | Status |
|-----|-------|------|-----------|--------|
| [KPI 1] | X | Y | ↑↓→ | 🟢🟡🔴 |
| [KPI 2] | X | Y | ↑↓→ | 🟢🟡🔴 |
| [KPI 3] | X | Y | ↑↓→ | 🟢🟡🔴 |

## Por Área

### Comercial
| KPI | Valor | Meta |
|-----|-------|------|
| [métricas de vendas] | | |

### Marketing
| KPI | Valor | Meta |
|-----|-------|------|
| [métricas de marketing] | | |

### Produto/Operações
| KPI | Valor | Meta |
|-----|-------|------|
| [métricas de produto] | | |

### Financeiro
| KPI | Valor | Meta |
|-----|-------|------|
| [métricas financeiras] | | |

## Rotina de Acompanhamento
- **Diário:** [métricas operacionais]
- **Semanal:** [pipeline, conversão, tráfego]
- **Mensal:** [financeiro, KPIs estratégicos, review]
- **Trimestral:** [OKRs, planning, forecast]
```

## Regras
- Máximo 7 KPIs no dashboard principal (mais = paralisia)
- Todo KPI precisa de meta definida (sem meta não é KPI, é dado)
- North Star Metric: 1 métrica que reflete o valor entregue ao cliente
- KPIs de vaidade (seguidores, pageviews isolados) ficam fora do dashboard principal
- Defina frequência de revisão para cada métrica
- Se não mede, não gerencia — mas se mede demais, também não gerencia

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-diagnostico` — use o output como input se já foi rodada
- `/whatsapp-crm` — use o output como input se já foi rodada

### Passa o bastão para:
- **KPIs definidos → dashboard** → `/ops-dados`
- **KPIs alimentam forecast** → `/negocios-forecasting`

### Contexto compartilhado
KPIs devem refletir os gargalos do diagnóstico. North Star Metric conecta tudo.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
