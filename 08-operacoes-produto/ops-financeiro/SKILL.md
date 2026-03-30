---
name: ops-financeiro
description: Gerencia operações financeiras — DRE, fluxo de caixa, budget, controle de custos e análise de margens. Use quando o usuário pedir para organizar financeiro, criar DRE, fluxo de caixa, orçamento, budget, análise financeira, controle de custos, margem de contribuição, ou planejamento financeiro.
---

# Operações Financeiras

Estruture controles financeiros claros para tomada de decisão.

## Entregáveis

### DRE Gerencial (Demonstrativo de Resultados)

```markdown
## DRE — [Empresa] — [Mês/Ano]

| Item | Valor | % Receita |
|------|-------|-----------|
| **Receita Bruta** | R$ X | 100% |
| (-) Impostos (Simples/LN/LP) | R$ X | X% |
| (-) Gateway/taxas | R$ X | X% |
| (-) Comissões/afiliados | R$ X | X% |
| = **Receita Líquida** | R$ X | X% |
| (-) Custo de entrega (COGS) | R$ X | X% |
| = **Margem Bruta** | R$ X | X% |
| (-) Marketing/Ads | R$ X | X% |
| (-) Equipe | R$ X | X% |
| (-) Ferramentas/SaaS | R$ X | X% |
| (-) Infraestrutura | R$ X | X% |
| (-) Administrativo | R$ X | X% |
| = **EBITDA** | R$ X | X% |
| (-) Pró-labore | R$ X | X% |
| = **Resultado Líquido** | **R$ X** | **X%** |
```

### Fluxo de Caixa

```markdown
## Fluxo de Caixa — [Mês/Ano]

| Semana | Entradas | Saídas | Saldo | Acumulado |
|--------|----------|--------|-------|-----------|
| S1 | R$ X | R$ X | R$ X | R$ X |
| S2 | R$ X | R$ X | R$ X | R$ X |
| S3 | R$ X | R$ X | R$ X | R$ X |
| S4 | R$ X | R$ X | R$ X | R$ X |

**Saldo inicial:** R$ X
**Saldo final:** R$ X
**Variação:** R$ X (+/-X%)
```

### Budget Anual

```markdown
## Budget [Ano]

| Categoria | Jan | Fev | Mar | ... | Total |
|-----------|-----|-----|-----|-----|-------|
| Receita | R$X | R$X | R$X | | R$X |
| Marketing | R$X | R$X | R$X | | R$X |
| Equipe | R$X | R$X | R$X | | R$X |
| Ferramentas | R$X | R$X | R$X | | R$X |
| **Resultado** | R$X | R$X | R$X | | R$X |
```

### Unit Economics

```markdown
## Unit Economics — [Produto]

| Métrica | Valor | Status |
|---------|-------|--------|
| Ticket Médio | R$ X | — |
| COGS por unidade | R$ X | — |
| Margem Bruta/unidade | R$ X (X%) | 🟢>60% |
| CAC | R$ X | — |
| LTV | R$ X | — |
| LTV/CAC | Xx | 🟢>3x |
| Payback | X meses | 🟢<12 |
| Break-even (unidades) | X | — |
```

## Regras
- DRE gerencial ≠ DRE contábil. O gerencial é para decisão, o contábil é para compliance
- Sempre calcule margem em % da receita (permite comparação entre períodos)
- Fluxo de caixa semanal para negócios < R$100K/mês, mensal para maiores
- Separe custos fixos de variáveis (crucial para entender alavancagem)
- Marketing como % da receita: <30% para negócios maduros, <50% em fase de crescimento
- Margem bruta < 50% = modelo de negócio precisa ser revisado
- Nunca tome decisão baseado só em faturamento — lucro e caixa são o que importam

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/meta-analise-campanha` — use o output como input se já foi rodada
- `/lancamento-metricas` — use o output como input se já foi rodada
- `/negocios-diagnostico` — use o output como input se já foi rodada

### Passa o bastão para:
- **Margem ruim → rever precificação** → `/negocios-precificacao`
- **DRE → forecast** → `/negocios-forecasting`
- **Budget → campanhas** → `/marketing-campanha`

### Contexto compartilhado
Investimento em ads e receita de lançamentos devem entrar no DRE automaticamente.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
