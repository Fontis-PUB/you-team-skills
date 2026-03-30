---
name: ops-cs
description: Estrutura operações de Customer Success — onboarding de clientes, health score, playbooks de retenção, NPS e gestão de churn. Use quando o usuário pedir para criar processo de CS, customer success, onboarding de cliente, health score, reduzir churn, pesquisa NPS, ou gestão de retenção de clientes.
---

# Customer Success

Estruture operações de CS que retêm clientes e expandem receita.

## Frameworks

### Health Score do Cliente

| Dimensão | Peso | Indicador | Score |
|----------|------|-----------|-------|
| Uso do produto | 30% | Logins, features usadas | 0-100 |
| Engajamento | 20% | Respostas, participação | 0-100 |
| Satisfação | 20% | NPS, CSAT, tickets | 0-100 |
| Financeiro | 15% | Pagamentos em dia, upgrade | 0-100 |
| Relacionamento | 15% | Reuniões, comunicação | 0-100 |

**Score Final:** Média ponderada → 🟢 Saudável (70-100) | 🟡 Atenção (40-69) | 🔴 Risco (0-39)

### Playbook por Estágio

**Onboarding (D1-D30)**
- Kickoff call + definição de metas
- Setup técnico + treinamento
- Quick win (primeiro resultado visível)
- Check-in semanal

**Adoção (D30-D90)**
- Expansão de uso (novas features)
- Business review mensal
- Coleta de feedback

**Retenção (ongoing)**
- QBR (Quarterly Business Review)
- NPS periódico
- Identificação de expansão (upsell/cross-sell)

**Risco de Churn**
- Trigger: health score < 40 ou sinal de insatisfação
- Ação imediata: contato do CS manager
- Escalation: envolver liderança se necessário
- Save plan: desconto, feature, suporte extra

## Output

```markdown
# 🎯 Playbook de CS — [Produto/Empresa]

## Jornada do Cliente

| Fase | Período | Objetivo | KPI | Responsável |
|------|---------|----------|-----|-------------|
| Onboarding | D1-30 | Ativação | Time-to-value | CS |
| Adoção | D30-90 | Engajamento | Feature adoption | CS |
| Valor | D90+ | Resultado | Health score | CS |
| Expansão | D180+ | Crescimento | NRR | CS + Sales |
| Renovação | T-60d | Retenção | Churn rate | CS |

## Health Score
[Tabela com dimensões, pesos e indicadores]

## Alertas e Ações

| Alerta | Trigger | Ação | SLA |
|--------|---------|------|-----|
| 🔴 Churn risk | Score < 40 | Contato urgente | 24h |
| 🟡 Low usage | Login < 1x/semana | Email + check-in | 48h |
| 🟡 Ticket aberto | > 48h sem resolução | Escalation | Imediato |
| 🟢 Expansion ready | Score > 80 + uso alto | Apresentar upgrade | Próximo QBR |

## Templates

### Email de Check-in Mensal
[Template]

### Agenda de QBR
1. Resultados do trimestre
2. Metas vs realizado
3. Roadmap de produto
4. Oportunidades de expansão
5. Próximos passos

### Pesquisa NPS
"Em uma escala de 0 a 10, qual a probabilidade de recomendar [produto] para um colega?"
+ Pergunta aberta: "O que motivou sua nota?"
```

## Regras
- Time-to-value < 14 dias (se demorar mais, churn aumenta drasticamente)
- NPS: rodar a cada 90 dias (não mais frequente)
- Detratores (0-6): contato pessoal em 24h
- Promotores (9-10): pedir depoimento/referral
- Health score deve ser automatizado (não manual)
- QBR trimestral obrigatório para clientes enterprise
- Churn evitado > churn salvo (previna, não remedie)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/comercial-follow-up` — use o output como input se já foi rodada
- `/lancamento-pos-venda` — use o output como input se já foi rodada

### Passa o bastão para:
- **NPS alto → pedir depoimento** → `/instagram-copy`
- **NPS baixo → retenção urgente** → `/whatsapp-atendimento`
- **Churn → análise** → `/ops-dados`
- **Expansion → comercial** → `/comercial-proposta`

### Contexto compartilhado
Depoimentos de clientes satisfeitos alimentam prova social em todas as skills de comunicação.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
