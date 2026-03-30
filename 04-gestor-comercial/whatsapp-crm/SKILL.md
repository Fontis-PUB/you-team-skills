---
name: whatsapp-crm
description: Organiza pipeline de vendas e gestão de leads via WhatsApp com etiquetas, funil e acompanhamento. Use quando o usuário pedir para organizar leads no WhatsApp, criar pipeline de vendas, sistema de etiquetas, gestão de contatos comerciais, ou funil de vendas via WhatsApp.
---

# WhatsApp CRM

Estruture um sistema de gestão de leads e pipeline de vendas usando WhatsApp Business.

## Estrutura de Pipeline

### Etapas do Funil

| Etapa | Etiqueta/Cor | Critério | Ação |
|-------|-------------|----------|------|
| Novo Lead | 🔵 Azul | Primeiro contato | Responder em 5min |
| Qualificado | 🟢 Verde | Passou BANT | Enviar proposta |
| Proposta Enviada | 🟡 Amarelo | Aguardando decisão | Follow-up em 48h |
| Negociação | 🟠 Laranja | Pediu desconto/condição | Apresentar alternativas |
| Fechado Ganho | ✅ Verde escuro | Pagou | Onboarding |
| Fechado Perdido | 🔴 Vermelho | Recusou | Registrar motivo |
| Reativação | 🟣 Roxo | Inativo 30d+ | Campanha de reativação |

## Rotina de Gestão

```markdown
# 📊 Dashboard WhatsApp CRM — [Empresa]

## Pipeline Atual

| Etapa | Quantidade | Valor Potencial | Ação Pendente |
|-------|-----------|-----------------|---------------|
| Novos | X | R$ X | Qualificar hoje |
| Qualificados | X | R$ X | Enviar proposta |
| Proposta | X | R$ X | Follow-up |
| Negociação | X | R$ X | Fechar |
| **Total Pipeline** | **X** | **R$ X** | — |

## Rotina Diária
- [ ] 08h: Responder leads novos (últimas 12h)
- [ ] 10h: Follow-up de propostas enviadas há 48h+
- [ ] 14h: Segundo contato com leads do dia
- [ ] 17h: Atualizar status de todos os leads ativos
- [ ] Sexta: Revisar pipeline completo + limpar perdidos

## Métricas Semanais
- Leads novos: X
- Taxa de qualificação: X% (meta: >40%)
- Taxa de proposta→fechamento: X% (meta: >25%)
- Tempo médio de resposta: Xmin (meta: <5min)
- Ticket médio: R$ X
- Receita fechada: R$ X
```

## Regras
- Lead sem resposta em 24h = lead morto (prioridade máxima: velocidade)
- Nunca deixe lead em "Proposta Enviada" por mais de 72h sem follow-up
- Registre o motivo de cada lead perdido (padrões revelam problemas no processo)
- Limite o pipeline ativo a 50 leads por vendedor (acima disso, qualidade cai)
- Leads perdidos entram em fluxo de reativação automático após 30 dias
- Revise e limpe o pipeline toda sexta-feira

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/whatsapp-atendimento` — use o output como input se já foi rodada
- `/whatsapp-chatbot` — use o output como input se já foi rodada

### Passa o bastão para:
- **Pipeline organizado → follow-up** → `/comercial-follow-up`
- **Dados alimentam forecast** → `/negocios-forecasting`
- **Métricas de conversão** → `/negocios-kpis`

### Contexto compartilhado
Pipeline é a fonte de verdade comercial. Forecast e KPIs puxam daqui.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
