---
name: lancamento-pos-venda
description: Estrutura o pós-venda de lançamentos — onboarding de alunos, pesquisa com não-compradores, sequência de retenção e preparação do próximo lançamento. Use quando o usuário mencionar pós-lançamento, onboarding de alunos, pesquisa pós-venda, retenção de alunos, downsell, order bump, ou preparação para relançamento.
---

# Pós-Venda de Lançamento

Estruture todo o pós-lançamento para maximizar retenção, reduzir reembolso e preparar o próximo ciclo.

## Fluxos Pós-Venda

### Para Compradores
1. **Email de boas-vindas** (imediato) — acesso + próximos passos claros
2. **Onboarding** (D1-D3) — tour pela plataforma, grupo, primeiro módulo
3. **Check-in** (D7) — "Como está sendo a experiência?"
4. **Engajamento** (D14) — destaque de vitórias de outros alunos
5. **Pesquisa NPS** (D30) — coletar depoimentos e feedback

### Para Não-Compradores
1. **Email de agradecimento** (D+1 pós-carrinho) — gratidão pelo engajamento
2. **Pesquisa** (D+2) — "O que faltou para você entrar?" (3-5 opções)
3. **Conteúdo de valor** (D+7) — manter relacionamento
4. **Downsell** (D+14, opcional) — oferta alternativa menor

### Para Boletos/PIX não pagos
1. **Lembrete** (D+1) — "Seu boleto vence amanhã"
2. **Reforço** (D+2) — benefícios + link para novo boleto
3. **Urgência** (D+3) — "Última chance de garantir"

## Debrief do Lançamento

```markdown
# 📋 Debrief — [Produto] — [Data]

## Números Finais
[Tabela de métricas consolidadas]

## O que funcionou
1. [Com dados]
2. [Com dados]

## O que não funcionou
1. [Com dados e hipótese]
2. [Com dados e hipótese]

## Insights para o Próximo
1. [Ação concreta]
2. [Ação concreta]

## Calendário Próximo Lançamento
- Data estimada: [X]
- Melhorias prioritárias: [lista]
```

## Regras
- Onboarding nos primeiros 48h reduz reembolso em até 50%
- Pesquisa com não-compradores é OURO — as objeções reais estão ali
- Nunca envie downsell antes de 7 dias pós-fechamento (parece desespero)
- Debrief deve acontecer em até 72h após fechamento do carrinho
- Colete depoimentos ativamente entre D7-D30 (quando o entusiasmo é maior)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/lancamento-emails-carrinho` — use o output como input se já foi rodada
- `/lancamento-metricas` — use o output como input se já foi rodada

### Passa o bastão para:
- **Onboarding → CS** → `/ops-cs`
- **Feedback de não-compradores → ajustar oferta** → `/lancamento-oferta`
- **Depoimentos → prova social** → `/instagram-copy`
- **Preparar próximo lançamento** → `/lancamento-cronograma`

### Contexto compartilhado
Dados de reembolso e NPS alimentam o próximo ciclo de lançamento.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
