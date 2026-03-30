---
name: lancamento-emails-carrinho
description: Cria sequências completas de emails para fase de carrinho aberto — abertura, valor, prova social, objeções, bônus, escassez e fechamento. Use quando o usuário pedir emails de vendas de lançamento, sequência de carrinho, emails de abertura/fechamento, emails de escassez, ou comunicações da fase de vendas de um lançamento digital.
---

# Emails de Carrinho (Fase de Vendas)

Crie a sequência completa de emails de vendas para carrinho aberto, com cada email focado em um gatilho mental específico.

## Sequência Padrão — Carrinho 7 Dias

| Dia | Email | Gatilho | Hora |
|-----|-------|---------|------|
| D1 | Carrinho aberto | Novidade + Oportunidade | 08h |
| D1 | Reforço | Visão do futuro | 19h |
| D2 | História/Caso | Prova Social | 10h |
| D3 | Método/Conteúdo | Autoridade + Valor | 10h |
| D4 | Objeções | Quebra de objeção | 10h |
| D5 | Bônus especial | Reciprocidade + Escassez | 10h |
| D6 | Penúltimo dia | Urgência | 10h |
| D6 | Noite | FOMO | 20h |
| D7 | Último dia | Deadline | 08h |
| D7 | Tarde | Prova + Urgência | 14h |
| D7 | Noite | Última chance | 20h |
| D7 | Final | "Fechando agora" | 23h |

## Framework por Email

### D1 — Abertura
- Assunto que gera curiosidade sobre a oferta
- Recap da transformação prometida nos CPLs
- Apresentação da oferta completa (o que inclui, bônus, garantia)
- CTA direto para página de vendas

### D2 — Prova Social
- Depoimento ou caso de sucesso em destaque
- Resultado específico com números
- "Se [pessoa] conseguiu, você também pode"
- CTA

### D3 — Autoridade/Valor
- Conteúdo extra que demonstra expertise
- "Isso é o que você aprende no módulo X"
- Demonstra profundidade sem entregar tudo
- CTA

### D4 — Objeções
- Aborde a objeção #1 do público diretamente
- Fórmula: "Sei que você pode estar pensando [objeção]... [resposta]"
- FAQ das 3 perguntas mais comuns
- Garantia como redutor de risco
- CTA

### D5 — Bônus
- Apresente bônus exclusivo (real, não fabricado)
- Bônus com prazo ("disponível apenas até D6")
- Ancoragem de valor: "Esse bônus sozinho vale R$X"
- CTA

### D6-D7 — Escassez/Urgência
- Countdown real
- Recap de tudo que a pessoa perde se não agir
- Depoimento rápido + link
- Último email: 3-5 linhas apenas, direto ao ponto

## Regras
- Cada email = 1 gatilho dominante (nunca misture prova social com escassez no mesmo email)
- Emails D1-D5: 200-400 palavras
- Emails D6-D7: progressivamente mais curtos (o último = 50-80 palavras)
- Assunto do último email deve ser urgente e curto ("Acabou", "Última chance [Nome]", "23:59")
- Sempre inclua link de descadastro visível
- Preheader text deve complementar o assunto, nunca repetir
- Para carrinho de 3 dias: comprima D1+D2, D4+D5, mantenha D7 completo
- Para carrinho de 5 dias: pule D3 e D6 manhã

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/lancamento-emails-cpl` — use o output como input se já foi rodada
- `/lancamento-oferta` — use o output como input se já foi rodada

### Passa o bastão para:
- **Carrinho fechado → pós-venda** → `/lancamento-pos-venda`
- **Métricas de conversão** → `/lancamento-metricas`

### Contexto compartilhado
A oferta, bônus e garantia devem ser idênticos ao definido em `/lancamento-oferta`.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
