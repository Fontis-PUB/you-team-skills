---
name: marketing-email
description: Cria estratégias e sequências de email marketing — newsletters, automações, nutrição, reengajamento e vendas. Use quando o usuário pedir email marketing, sequência de emails, newsletter, automação de email, fluxo de nutrição, email de boas-vindas, ou estratégia de email.
---

# Email Marketing

Crie estratégias e sequências de email que nutrem, engajam e convertem.

## Tipos de Sequência

### Welcome Series (5-7 emails em 14 dias)
1. Boas-vindas + entrega do lead magnet
2. História/origem (quem somos)
3. Conteúdo de valor #1 (quick win)
4. Prova social (cases/depoimentos)
5. Conteúdo de valor #2
6. Soft pitch (apresentação da oferta)
7. CTA direto

### Nutrição (ongoing, 1-2x/semana)
- 80% valor, 20% venda
- Alternar: educativo, storytelling, curadoria, prova social, oferta

### Reengajamento (para inativos 60d+)
1. "Sentimos sua falta" + conteúdo irresistível
2. Pesquisa: "O que gostaria de receber?"
3. Oferta exclusiva de retorno
4. Último email: "Vamos te remover da lista" (reverse psychology)

### Abandono de Carrinho
1. +1h: Lembrete amigável
2. +24h: Prova social + urgência leve
3. +72h: Incentivo (desconto ou bônus)

## Estrutura de Email

```
ASSUNTO: [máx 50 chars — testado]
PREHEADER: [máx 90 chars — complementar]

[Saudação pessoal]

[Hook — 1-2 linhas que prendem]

[Corpo — 3-5 parágrafos curtos]
[Valor, história ou argumento]

[CTA — 1 ação clara, botão ou link]

[P.S. — segundo gancho ou CTA alternativo]
```

## Output

```markdown
# 📧 Sequência de Email — [Nome]
**Tipo:** [welcome/nutrição/venda/reengajamento]
**Frequência:** [X emails em Y dias]
**Objetivo:** [nutrição/conversão/retenção]

## Email 1 — [Tema]
**Envio:** [D+X ou trigger]
**Assunto:** [texto]
**Preheader:** [texto]
**Corpo:**
[copy completo]
**CTA:** [ação + link]

[Repetir para cada email]

## Métricas Alvo
- Open rate: >25%
- CTR: >3%
- Unsubscribe: <0.5%
```

## Regras
- Assuntos: teste A/B sempre (mínimo 2 variações)
- Personalização: use nome + segmentação quando possível
- Mobile: 65%+ abrem no celular — parágrafos curtos, CTA grande
- Frequência: 2-3x/semana máx (mais = mais unsubscribe)
- Segmente por engajamento (ativos vs. inativos) — mensagem diferente
- Nunca compre lista — só envie para opt-in
- Limpe lista a cada 90 dias (remova bounces e inativos 180d+)
- Melhor horário BR: terça-quinta, 8-10h ou 19-21h

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-funil` — use o output como input se já foi rodada
- `/marketing-persona` — use o output como input se já foi rodada

### Passa o bastão para:
- **Leads aquecidos → comercial** → `/whatsapp-atendimento`
- **Sequência de lançamento** → `/lancamento-emails-cpl`

### Contexto compartilhado
Segmentação por engajamento. Tom alinhado com persona e brand voice.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
