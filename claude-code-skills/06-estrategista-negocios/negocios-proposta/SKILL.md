---
name: negocios-proposta
description: Cria propostas de consultoria e projetos estratégicos com diagnóstico, escopo, metodologia e investimento. Use quando o usuário pedir proposta de consultoria, escopo de projeto estratégico, proposta de assessment, ou documento formal de engajamento B2B de consultoria/advisory.
---

# Proposta de Consultoria

Crie propostas de consultoria/advisory que demonstram expertise e justificam o investimento.

## Estrutura

```markdown
# Proposta de Consultoria Estratégica
**Para:** [Cliente]
**De:** [Consultoria]
**Data:** [dd/mm/yyyy]

## 1. Entendimento do Contexto
[Demonstre que entendeu a situação, desafios e ambições do cliente — 3-4 parágrafos]

## 2. Diagnóstico Preliminar
[Observações e hipóteses sobre os gargalos/oportunidades — baseado em discovery]

## 3. Escopo e Metodologia

### Fase 1: Diagnóstico (X semanas)
- [Atividades: entrevistas, análise de dados, benchmark]
- **Entregável:** Relatório de diagnóstico + apresentação

### Fase 2: Estratégia (X semanas)
- [Atividades: workshops, definição de roadmap]
- **Entregável:** Plano estratégico + priorização

### Fase 3: Implementação Assistida (X semanas)
- [Atividades: acompanhamento, mentorias, ajustes]
- **Entregável:** Dashboards, processos, documentação

## 4. Equipe
| Consultor | Papel | Dedicação |
|-----------|-------|-----------|
| [nome] | Lead | X h/semana |
| [nome] | Especialista | X h/semana |

## 5. Investimento e Condições
| Fase | Duração | Investimento |
|------|---------|-------------|
| Diagnóstico | X semanas | R$ X |
| Estratégia | X semanas | R$ X |
| Implementação | X semanas | R$ X/mês |
| **Total** | **X semanas** | **R$ X** |

**Condições:** [pagamento, parcelamento]

## 6. Resultados Esperados
- [Resultado tangível com métrica]
- [Resultado tangível com métrica]

## 7. Próximos Passos
1. Aprovação e assinatura
2. Kickoff em [data]
3. Primeiro entregável em [data]
```

## Regras
- Diagnóstico deve demonstrar que você já pensou sobre o problema (não é genérico)
- Metodologia proprietária (se tiver) diferencia da concorrência
- Sempre inclua entregáveis concretos por fase
- Investimento ancorado no resultado, não nas horas
- Proposta de consultoria ≠ proposta de serviço operacional (o tom é advisory)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-diagnostico` — use o output como input se já foi rodada
- `/negocios-precificacao` — use o output como input se já foi rodada

### Passa o bastão para:
- **Proposta aceita → cronograma** → `/negocios-processos`
- **Proposta aceita → KPIs** → `/negocios-kpis`

### Contexto compartilhado
Use o diagnóstico como base da seção de contexto da proposta.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
