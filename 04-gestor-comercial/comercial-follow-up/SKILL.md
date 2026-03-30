---
name: comercial-follow-up
description: Cria sequências de follow-up comercial multicanal com timing, mensagens e escalation. Use quando o usuário pedir templates de follow-up, sequência de acompanhamento, cadência de vendas, mensagens de retorno, ou como fazer follow-up sem ser inconveniente.
---

# Follow-up Comercial

Crie cadências de follow-up que convertem sem queimar o lead.

## Cadência Padrão (7 touchpoints em 21 dias)

| # | Dia | Canal | Tipo | Objetivo |
|---|-----|-------|------|----------|
| 1 | D0 | WhatsApp | Mensagem | Agradecer + próximo passo |
| 2 | D2 | Email | Valor | Conteúdo relevante |
| 3 | D5 | WhatsApp | Check-in | "Viu minha mensagem?" |
| 4 | D7 | Email | Case/Prova | Resultado de cliente similar |
| 5 | D10 | WhatsApp | Direto | Pergunta sobre decisão |
| 6 | D14 | Email | Objeção | Antecipar dúvidas comuns |
| 7 | D21 | WhatsApp | Breakup | "Última tentativa" |

## Templates por Situação

### Pós-Reunião (sem resposta)
**D+2:** "Oi [Nome], tudo bem? Enviei a proposta [dia]. Ficou alguma dúvida?"
**D+5:** "Oi [Nome], sei que a semana é corrida. Queria saber se conseguiu analisar a proposta. Posso ajudar com algo?"
**D+10:** "Oi [Nome], quero respeitar seu tempo. Me diz: faz sentido continuarmos ou o momento não é esse?"

### Pós-Proposta (pediu tempo)
**D+3:** "[Nome], lembrei de um case parecido com sua situação: [resultado]. Acho que pode te ajudar na decisão."
**D+7:** "Oi [Nome], tenho uma condição especial que expira [data]. Quer que eu detalhe?"

### Breakup (última tentativa)
"[Nome], tentei te contatar algumas vezes e entendo que o momento pode não ser ideal. Vou parar de insistir, mas fico à disposição quando fizer sentido. É só me chamar."

## Output

```markdown
# 🔄 Cadência de Follow-up — [Produto/Contexto]

## Sequência

| # | Dia | Canal | Mensagem | Gatilho |
|---|-----|-------|----------|---------|
| 1 | D+0 | [canal] | "[texto exato]" | [contexto] |
| 2 | D+X | [canal] | "[texto exato]" | [contexto] |
[...]

## Regras de Escalation
- Se respondeu positivamente → avançar no pipeline
- Se pediu mais tempo → pausar 7d e retomar
- Se disse não → registrar motivo + mover para nurture
- Se não respondeu após 7 tentativas → breakup + nurture list

## Automação Sugerida
[Fluxo para configurar em ferramenta de automação]
```

## Regras
- Follow-up com VALOR > follow-up com cobrança ("lembrar" não é valor)
- Cada touchpoint deve trazer algo novo (case, dado, insight, condição)
- Máximo 7 tentativas antes do breakup — depois disso é assédio
- Alterne canais (WhatsApp → Email → WhatsApp)
- Breakup email tem taxa de resposta surpreendente (~30%) — sempre use
- Horários: WhatsApp 9-11h ou 14-16h / Email 8-10h
- Nunca envie follow-up em fim de semana para B2B
- Tom: consultivo e empático, nunca desesperado

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/comercial-proposta` — use o output como input se já foi rodada
- `/whatsapp-crm` — use o output como input se já foi rodada

### Passa o bastão para:
- **Lead converteu → CS** → `/ops-cs`
- **Lead perdido → reativação** → `/marketing-email`

### Contexto compartilhado
Cada touchpoint deve trazer valor novo. Use cases de `/ops-cs` como prova social nos follow-ups.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
