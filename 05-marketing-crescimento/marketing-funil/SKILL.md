---
name: marketing-funil
description: Mapeia e estrutura funis de marketing completos — desde atração até conversão e retenção, com canais, conteúdo e automações em cada etapa. Use quando o usuário pedir para criar funil de vendas, mapear jornada do cliente, estruturar funil de marketing, definir estratégia de aquisição, ou organizar o fluxo de conversão do negócio.
---

# Funil de Marketing

Estruture funis completos com estratégia, canais e métricas para cada etapa.

## Modelos de Funil

### Funil Clássico (TOFU → MOFU → BOFU)
- **Topo:** Atração e descoberta (conteúdo, SEO, ads, social)
- **Meio:** Consideração e nutrição (email, webinar, cases)
- **Fundo:** Decisão e conversão (oferta, trial, demo, proposta)

### Funil de Infoproduto
Tráfego → LP Captura → Nutrição/CPL → Página de Vendas → Checkout → Upsell → Entrega

### Funil SaaS
Tráfego → LP → Trial/Freemium → Onboarding → Ativação → Conversão Paga → Expansão → Advocacia

### Funil E-commerce
Tráfego → Categoria/Produto → Carrinho → Checkout → Pós-Compra → Recompra

### Funil de Serviços B2B
Conteúdo/Ads → Lead Magnet → Qualificação → Reunião → Proposta → Negociação → Contrato

## Output

```markdown
# 🔄 Mapa de Funil — [Negócio]
**Modelo:** [tipo]
**Objetivo:** [X conversões/mês a R$ Y]

## Visão Geral do Funil

| Etapa | Canal | Conteúdo/Ação | Métrica | Meta |
|-------|-------|---------------|---------|------|
| Topo | [canais] | [tipo conteúdo] | [impressões/alcance] | [X] |
| Meio | [canais] | [tipo conteúdo] | [leads/engajamento] | [X] |
| Fundo | [canais] | [tipo conteúdo] | [conversões] | [X] |
| Retenção | [canais] | [tipo conteúdo] | [LTV/NRR] | [X] |

## Detalhamento por Etapa

### Topo — Atração
**Objetivo:** Gerar [X] visitantes/mês
**Canais:** [lista com % de investimento]
**Conteúdo:** [tipos de conteúdo]
**KPIs:** CPM, alcance, tráfego
**Automação:** [o que automatizar]

### Meio — Nutrição
[mesma estrutura]

### Fundo — Conversão
[mesma estrutura]

### Pós — Retenção e Expansão
[mesma estrutura]

## Calculadora de Funil (de trás para frente)

| Etapa | Volume | Taxa de Conversão | Resultado |
|-------|--------|-------------------|-----------|
| Meta de receita | — | — | R$ X |
| Clientes necessários | X | — | X clientes |
| Propostas/ofertas | X | Conv X% | X propostas |
| Leads qualificados | X | Qualif X% | X SQLs |
| Leads captados | X | Captura X% | X leads |
| Tráfego necessário | X | CTR X% | X visitas |
| Investimento estimado | — | CPC R$ X | R$ X/mês |
```

## Regras
- Sempre calcule o funil de trás para frente (meta de receita → tráfego necessário)
- Cada etapa deve ter métrica clara e conversão esperada
- Identifique o maior gargalo e priorize (80/20)
- Retenção é mais barato que aquisição — sempre inclua essa camada
- Para SaaS: foque em ativação e expansão (NRR > new logo revenue)
- Funil sem automação não escala — inclua recomendações de automação

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-persona` — use o output como input se já foi rodada
- `/negocios-diagnostico` — use o output como input se já foi rodada

### Passa o bastão para:
- **Topo precisa de tráfego** → `/meta-analise-campanha`
- **Meio precisa de conteúdo** → `/instagram-calendario`
- **Fundo precisa de comercial** → `/whatsapp-atendimento`
- **Automação do funil** → `/ops-automacao`

### Contexto compartilhado
O funil é o mapa mestre de aquisição. Todas as skills de tráfego, conteúdo e comercial operam dentro dele.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
