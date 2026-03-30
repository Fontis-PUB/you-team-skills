---
name: google-relatorio
description: Gera relatórios profissionais de performance de campanhas Google Ads para clientes e stakeholders. Use quando o usuário pedir relatório de Google Ads, report de search/display/YouTube/PMax, resumo de performance Google, ou documentação de resultados de campanhas Google para apresentação.
---

# Google Relatório de Performance

Gere relatórios estruturados de campanhas Google Ads adaptados ao tipo de campanha e ao nível de conhecimento técnico do destinatário.

## Coleta

- Dados de performance (período, métricas)
- Tipo(s) de campanha
- Nome do cliente/projeto
- Comparativo desejado (período anterior, meta)
- Nível do destinatário (técnico vs. executivo)

## Estrutura do Output

```markdown
# Relatório Google Ads — [Cliente]
**Período:** [X]  |  **Investimento:** R$ [X]

## Resumo Executivo
[2-3 frases com resultado principal, comparação e próximo passo]

## Performance Consolidada

| Indicador | Atual | Anterior | Meta | Var. |
|-----------|-------|----------|------|------|
| Impressões | X | Y | — | +/-% |
| Cliques | X | Y | — | +/-% |
| CTR | X% | Y% | Z% | +/- p.p. |
| CPC Médio | R$X | R$Y | R$Z | +/-% |
| Conversões | X | Y | Z | +/-% |
| CPA | R$X | R$Y | R$Z | +/-% |
| ROAS | Xx | Yx | Zx | +/-% |
| Receita | R$X | R$Y | R$Z | +/-% |

## Performance por Campanha

### [Nome da Campanha] — [Tipo]
| Métrica | Valor |
|---------|-------|
[métricas específicas do tipo]

**Status:** 🟢 Escalar / 🟡 Otimizar / 🔴 Pausar
**Observação:** [contexto relevante]

## Top Keywords (Search)
| Keyword | Cliques | Conv. | CPA | QS |
|---------|---------|-------|-----|----|
[top 10 por conversão]

## Destaques e Aprendizados
1. [Insight acionável]
2. [Insight acionável]

## Plano — Próximo Período
- [ ] [Ação 1]
- [ ] [Ação 2]
- [ ] [Ação 3]
```

## Regras
- Para clientes não-técnicos, omita Quality Score e Search Terms — foque em resultado de negócio (leads, vendas, ROAS)
- Sempre compare com período anterior E com meta (se definida)
- Destaque economia ou ganho incremental em reais quando possível
- PMax: informe a limitação de visibilidade por canal — seja transparente

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/google-analise-campanha` — use o output como input se já foi rodada

### Passa o bastão para:
- **Precisa otimizar keywords** → `/conteudo-pauta-seo`
- **Budget review** → `/ops-financeiro`

### Contexto compartilhado
Se já existe relatório de Meta, consolide em visão unificada de tráfego pago.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
