---
name: whatsapp-disparos
description: Cria campanhas de disparo em massa para WhatsApp — listas de transmissão, mensagens segmentadas e sequências automatizadas. Use quando o usuário pedir templates de disparo, mensagens em massa, campanhas de WhatsApp, lista de transmissão, ou comunicação em escala via WhatsApp Business/API.
---

# WhatsApp Disparos

Crie campanhas de mensagens em massa segmentadas e eficazes.

## Tipos de Disparo

### Promoção/Oferta
- Gatilho: nova oferta, desconto, lançamento
- Mensagem curta + imagem + link
- Melhor dia: terça a quinta, 10h-12h ou 18h-20h

### Conteúdo/Nutrição
- Gatilho: novo conteúdo, dica, novidade
- Formato: texto + link ou vídeo curto

### Reativação
- Gatilho: cliente inativo há 30-90 dias
- Tom pessoal: "Faz tempo que não te vejo por aqui"

### Carrinho Abandonado
- Gatilho: abandono há 1h, 24h, 72h
- Progressão: lembrete → incentivo → urgência

### Pós-Venda
- Gatilho: compra realizada há X dias
- Objetivo: NPS, cross-sell, indicação

## Output

```markdown
# 📤 Campanha WhatsApp — [Nome]

## Segmento: [descrição do público]
## Objetivo: [venda/reativação/nutrição]
## Volume estimado: [X contatos]

### Mensagem Principal
"[texto — máx 160 caracteres para preview]"

[Complemento se necessário — máx 3 linhas]

[CTA + link]

### Imagem/Mídia
[Descrição da imagem ou vídeo a acompanhar]

### Variação B (teste)
"[versão alternativa]"

---

## Segmentação Recomendada

| Lista | Critério | Volume | Mensagem |
|-------|----------|--------|----------|
| VIP | Comprou 2+ vezes | ~X | Oferta exclusiva |
| Leads quentes | Engajou 30d | ~X | Conteúdo + CTA |
| Inativos | Sem interação 60d+ | ~X | Reativação |

## Cronograma de Envio

| Dia | Hora | Lista | Mensagem |
|-----|------|-------|----------|
| [dia] | [hora] | [lista] | [msg] |
```

## Regras
- Máximo 160 caracteres na primeira mensagem (preview no push notification)
- Nunca dispare para quem não optou in (LGPD + risco de ban)
- Frequência máxima: 2-3 disparos/semana por contato
- Segmente SEMPRE — disparo genérico = alta taxa de bloqueio
- Inclua opção de descadastro ("Digite SAIR para não receber mais")
- Melhor horário BR: terça-quinta, 10h-12h ou 18h-20h
- Evite segunda (início de semana) e sexta (fim de semana)
- Para API: respeite os templates aprovados pelo Meta

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/whatsapp-crm` — use o output como input se já foi rodada
- `/marketing-email` — use o output como input se já foi rodada

### Passa o bastão para:
- **Respostas entram no pipeline** → `/whatsapp-crm`

### Contexto compartilhado
Segmentação deve seguir as listas do CRM. Tom e oferta devem ser consistentes com email marketing.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
