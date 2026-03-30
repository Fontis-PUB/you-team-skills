---
name: negocios-precificacao
description: Define estratégias de precificação — análise de custos, valor percebido, posicionamento competitivo e modelos de pricing. Use quando o usuário pedir para definir preço, estratégia de precificação, pricing, modelo de cobrança, ou avaliar se o preço atual está correto.
---

# Precificação

Defina preços baseados em custo, valor percebido e posicionamento competitivo.

## Métodos de Precificação

### 1. Cost-Plus (Custo + Margem)
- Custo total (fixo + variável) + margem desejada
- Simples mas ignora o que o mercado aceita pagar
- Usar como piso (preço mínimo viável)

### 2. Baseado em Valor
- Quanto vale o resultado para o cliente?
- Se você economiza R$10K/mês para o cliente, pode cobrar R$2-3K
- Melhor para serviços e SaaS

### 3. Competitivo
- Posicionar em relação aos concorrentes
- Premium (acima), paridade (igual), penetração (abaixo)

### 4. Modelos de Pricing

| Modelo | Melhor para | Exemplo |
|--------|------------|---------|
| Único | Produtos, cursos | R$ 997 |
| Assinatura | SaaS, memberships | R$ 97/mês |
| Freemium | SaaS, apps | Free → R$ 49/mês |
| Tiered | SaaS, serviços | Basic/Pro/Enterprise |
| Usage-based | APIs, infra | R$ 0.01/request |
| Retainer | Consultoria, agência | R$ 5K/mês |
| Success fee | Vendas, performance | % do resultado |

## Output

```markdown
# 💰 Estratégia de Precificação — [Produto/Serviço]

## Análise de Custo (Piso)
| Item | Custo Mensal/Unitário |
|------|----------------------|
| [custo fixo] | R$ X |
| [custo variável] | R$ X |
| **Total** | **R$ X** |
| Margem mínima (30%) | R$ X |
| **Preço mínimo** | **R$ X** |

## Análise de Valor (Teto)
- Problema que resolve: [X]
- Valor do problema para o cliente: R$ [X]/mês
- Preço máximo (20-30% do valor): R$ [X]

## Análise Competitiva
| Concorrente | Preço | Modelo | Posicionamento |
|-------------|-------|--------|---------------|
| [X] | R$ X | [X] | [X] |

## Recomendação

**Modelo:** [X]
**Preço sugerido:** R$ [X]
**Justificativa:** [por que este preço]

### Planos (se tiered)
| Plano | Inclui | Preço | Público |
|-------|--------|-------|---------|
| [Basic] | [X] | R$ X | [X] |
| [Pro] | [X] | R$ X | [X] |
| [Enterprise] | [X] | R$ X | [X] |

## Psicologia de Preço
- Ancoragem: mostrar plano premium primeiro
- Charm pricing: R$ 997 vs R$ 1.000
- Desconto à vista PIX: R$ X (incentiva cash flow)
```

## Regras
- Preço baseado em custo = piso. Preço baseado em valor = teto. Posicione entre os dois.
- Para SaaS: 3 planos, o do meio deve ser o mais atrativo (decoy effect)
- Nunca precifique sem conhecer custos E o que concorrentes cobram
- Desconto deve ter motivo (prazo, volume, fidelidade) — nunca "porque sim"
- Teste preço antes de fixar — price sensitivity research com público real
- Para serviços: precifique por valor entregue, não por hora (evita race to the bottom)
- Revise preços a cada 6-12 meses (inflação, custos, posicionamento)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-concorrentes` — use o output como input se já foi rodada
- `/ops-financeiro` — use o output como input se já foi rodada

### Passa o bastão para:
- **Preço definido → oferta** → `/lancamento-oferta`
- **Preço definido → proposta** → `/comercial-proposta`

### Contexto compartilhado
Custo vem de `/ops-financeiro`. Concorrência vem de `/marketing-concorrentes`. Valor vem da persona.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
