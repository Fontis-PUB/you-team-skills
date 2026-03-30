---
name: ops-automacao
description: Projeta automações de negócio com no-code/low-code (Make, Zapier, n8n) e APIs — fluxos, triggers, integrações e lógica condicional. Use quando o usuário pedir automação, integração entre ferramentas, fluxo automatizado, workflow, conexão entre sistemas, Make/Zapier/n8n, ou eliminar tarefas manuais repetitivas.
---

# Automação de Negócio

Projete automações que eliminam trabalho manual e conectam sistemas.

## Quando Automatizar

### Critérios
- Tarefa repetitiva (>3x/semana)
- Baseada em regras (if this, then that)
- Conecta 2+ ferramentas
- Tempo gasto > 30min/semana
- Erro humano frequente

### NÃO automatizar
- Decisões que requerem julgamento humano
- Processos que mudam toda semana
- Tasks feitas 1x/mês (custo > benefício)

## Ferramentas

| Ferramenta | Melhor para | Complexidade | Custo |
|-----------|------------|-------------|-------|
| Zapier | Automações simples, muitas integrações | Baixa | $$$ |
| Make (Integromat) | Fluxos complexos, lógica avançada | Média | $$ |
| n8n | Self-hosted, controle total, código | Alta | $ (self-hosted) |
| APIs diretas | Performance, customização total | Alta | $-$$$ |

## Automações Comuns por Área

### Comercial
- Lead entra no CRM → notificação WhatsApp → tarefa para vendedor
- Proposta enviada → follow-up automático em 48h
- Deal fechado → NF gerada → onboarding triggered

### Marketing
- Post agendado → cross-post em múltiplas redes
- Lead captado → tag + sequência de email
- Formulário preenchido → lead scoring → roteamento

### Operações
- Pagamento confirmado → acesso liberado → email de boas-vindas
- Ticket de suporte → classificação → roteamento → SLA
- Report semanal → dados coletados → email enviado

### Financeiro
- NF emitida → registro no controle → notificação
- Pagamento recebido → baixa automática → conciliação
- Cobrança vencida → lembrete automático → escalation

## Output

```markdown
# ⚡ Automação — [Nome do Fluxo]
**Ferramenta:** [Make/Zapier/n8n/API]
**Trigger:** [o que inicia o fluxo]
**Frequência:** [tempo real / polling Xmin / scheduled]

## Visão Geral do Fluxo

[Trigger] → [Step 1] → [Decisão?]
                            ├─ Sim → [Step 2A] → [Step 3]
                            └─ Não → [Step 2B]

## Detalhamento

### Step 1: [Nome]
- **App:** [ferramenta]
- **Ação:** [o que faz]
- **Input:** [dados que recebe]
- **Output:** [dados que passa adiante]

### Step 2: [Nome]
[mesma estrutura]

### Condição: [Descrição]
- **Se:** [condição]
- **Então:** [caminho A]
- **Senão:** [caminho B]

## Tratamento de Erros
| Erro | Causa | Ação |
|------|-------|------|
| [erro] | [causa] | [retry/skip/alert] |

## Monitoramento
- **Alertas:** [quando notificar — falha, volume anormal]
- **Logs:** [onde registrar execuções]
- **Review:** [frequência de revisão do fluxo]

## ROI da Automação
- **Tempo manual eliminado:** X horas/mês
- **Custo da ferramenta:** R$ X/mês
- **Economia líquida:** R$ X/mês (ou X horas)
```

## Regras
- Comece simples (2-3 steps) e expanda depois
- SEMPRE inclua tratamento de erro (fluxos quebram — quando, não se)
- Teste com dados reais antes de ativar
- Documente cada fluxo (daqui 6 meses ninguém vai lembrar a lógica)
- Monitore execuções — automação silenciosa que falha é pior que processo manual
- Calcule ROI: se não economiza tempo ou dinheiro mensurável, não automatize
- Para Make/Zapier: cuidado com limites de operações do plano

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-processos` — use o output como input se já foi rodada
- `/marketing-funil` — use o output como input se já foi rodada

### Passa o bastão para:
- **Automação implementada → documentar** → `/ops-documentacao`

### Contexto compartilhado
Automatize processos mapeados em `/negocios-processos` e etapas do funil.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
