---
name: comercial-crm
description: Estrutura e organiza sistemas de CRM comercial — pipeline, etapas, campos, automações e relatórios. Use quando o usuário pedir para configurar CRM, organizar funil de vendas, definir etapas do pipeline, criar campos personalizados, ou estruturar processo comercial.
---

# CRM Comercial

Estruture o processo comercial com pipeline, automações e métricas.

## Estrutura do Pipeline

### Etapas Padrão B2B
1. **Lead Novo** → Qualificação em 24h
2. **MQL (Marketing Qualified)** → Atende critérios mínimos
3. **SQL (Sales Qualified)** → Passou BANT, tem fit
4. **Reunião Agendada** → Discovery call marcada
5. **Proposta Enviada** → Aguardando decisão
6. **Negociação** → Ajustes de escopo/preço
7. **Fechado Ganho** → Contrato assinado
8. **Fechado Perdido** → Motivo registrado

### Etapas Padrão B2C/Infoproduto
1. **Lead** → Captado via LP/anúncio
2. **Engajado** → Abriu email / respondeu WhatsApp
3. **Qualificado** → Demonstrou interesse real
4. **Oportunidade** → Viu oferta/página de vendas
5. **Comprou** → Pagamento confirmado
6. **Não Comprou** → Motivo + fluxo de nutrição

## Campos Essenciais por Lead

| Campo | Tipo | Obrigatório | Uso |
|-------|------|-------------|-----|
| Nome | Texto | Sim | Identificação |
| Email | Email | Sim | Comunicação |
| Telefone/WhatsApp | Telefone | Sim | Contato direto |
| Origem | Dropdown | Sim | Atribuição de canal |
| Produto de Interesse | Dropdown | Sim | Segmentação |
| Valor Estimado | Moeda | Não | Forecast |
| Próxima Ação | Texto | Sim | Follow-up |
| Data Próxima Ação | Data | Sim | Agenda |
| Motivo de Perda | Dropdown | Condicional | Análise |

## Métricas do CRM

```markdown
## Dashboard Comercial — [Período]

### Pipeline
| Etapa | Leads | Valor | Conversão p/ próx. |
|-------|-------|-------|---------------------|
| [cada etapa] | X | R$ X | X% |

### Velocidade de Vendas
- Tempo médio lead→fechamento: X dias
- Tempo médio por etapa: [breakdown]
- Gargalo: [etapa com maior tempo]

### Performance
- Win rate: X%
- Ticket médio: R$ X
- Receita fechada: R$ X
- Meta: R$ X (X% atingido)

### Motivos de Perda (Top 5)
1. [motivo] — X%
2. [motivo] — X%
3. [motivo] — X%
```

## Regras
- Todo lead precisa de "Próxima Ação" com data — pipeline parado = lead morto
- Motivo de perda é obrigatório — sem isso, não há melhoria
- Revise pipeline semanalmente (pipeline review)
- Leads parados há 14d+ em qualquer etapa → ação forçada ou arquivo
- Origem do lead SEMPRE registrada (essencial para calcular CAC por canal)
- Para SaaS: adicione campos de MRR estimado e ciclo de contrato

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/whatsapp-crm` — use o output como input se já foi rodada
- `/comercial-proposta` — use o output como input se já foi rodada

### Passa o bastão para:
- **Motivos de perda → ajustar oferta** → `/lancamento-oferta`
- **Motivos de perda → ajustar copy** → `/meta-copy-criativo`
- **Pipeline → forecast** → `/negocios-forecasting`

### Contexto compartilhado
Motivos de perda são ouro. Sempre faça a ponte com oferta e comunicação.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
