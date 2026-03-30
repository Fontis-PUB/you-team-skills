---
name: whatsapp-atendimento
description: Cria scripts de atendimento comercial via WhatsApp — abordagem, qualificação, quebra de objeções e fechamento. Use quando o usuário pedir script de WhatsApp, mensagens de atendimento, fluxo de vendas por WhatsApp, abordagem de lead, script de SDR/closer, ou templates de mensagens comerciais.
---

# WhatsApp Atendimento Comercial

Crie scripts de atendimento que qualificam e convertem leads via WhatsApp.

## Fases do Atendimento

### 1. Primeiro Contato (até 5 minutos após o lead entrar)
- Mensagem curta e personalizada
- Confirme o interesse/origem
- Faça uma pergunta aberta para iniciar conversa

### 2. Qualificação (BANT adaptado)
- **Budget:** Tem orçamento disponível?
- **Authority:** É o decisor?
- **Need:** Qual a dor/necessidade real?
- **Timeline:** Quando precisa resolver?

### 3. Apresentação de Valor
- Conecte a dor com a solução
- Use prova social rápida
- Não envie PDF/proposta antes de qualificar

### 4. Quebra de Objeções
- "Tá caro" → Ancoragem de valor + parcelamento
- "Vou pensar" → "O que falta para você decidir?"
- "Não é o momento" → "Quando seria? Posso te avisar?"
- "Vou falar com meu sócio/cônjuge" → "Posso ajudar com algum material?"

### 5. Fechamento
- Assunção de fechamento: "Vou gerar seu acesso então?"
- Alternativa: "Prefere à vista ou parcelado?"
- Link de pagamento direto na conversa

## Output

```markdown
# 💬 Script WhatsApp — [Produto/Serviço]

## Mensagem 1 — Primeiro Contato
"[texto — máx 3 linhas]"
⏱️ Enviar em: até 5 min após o lead

## Mensagem 2 — Qualificação
"[pergunta aberta]"
⏱️ Enviar: após resposta

## Mensagem 3 — Valor
"[conexão dor + solução + prova]"

## Mensagem 4 — Oferta
"[apresentação da oferta + condições]"

## Mensagem 5 — Fechamento
"[CTA direto + link]"

---

## Respostas para Objeções

**"Quanto custa?"** (antes de qualificar)
→ "[resposta que redireciona para qualificação]"

**"Está caro"**
→ "[resposta]"

**"Vou pensar"**
→ "[resposta]"

**"Não conheço a empresa"**
→ "[resposta com prova social]"

## Follow-up Automático

| Tempo | Mensagem | Objetivo |
|-------|----------|----------|
| +2h | "[lembrete suave]" | Reengajar |
| +24h | "[valor adicional]" | Nutrir |
| +72h | "[última tentativa]" | Fechar ou arquivar |
```

## Regras
- Máximo 3 linhas por mensagem (ninguém lê paredes de texto no WhatsApp)
- Nunca envie áudio no primeiro contato
- Responder em até 5 minutos = 5x mais chance de conversão
- Não envie proposta/preço sem antes qualificar
- Use o nome da pessoa em toda mensagem
- Emoji com moderação (1-2 por mensagem, profissional)
- Sempre termine com pergunta (mantém a conversa viva)
- Horário de envio: 08h-20h (respeite o horário do lead)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-persona` — use o output como input se já foi rodada
- `/marketing-funil` — use o output como input se já foi rodada

### Passa o bastão para:
- **Lead qualificado → proposta** → `/comercial-proposta`
- **Lead precisa de nurture** → `/comercial-follow-up`
- **Objeções recorrentes → ajustar oferta** → `/lancamento-oferta`

### Contexto compartilhado
O script deve falar a língua da persona. Se o funil está definido, adapte a abordagem ao estágio do lead.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
