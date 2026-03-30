---
name: lancamento-cronograma
description: Monta cronogramas completos de lançamento digital (PLF, Webinário, Desafio, Meteórico) com fases, datas, entregas e responsáveis. Use quando o usuário mencionar cronograma de lançamento, planejamento de lançamento, timeline, fases de lançamento (PPL, PL, carrinho), ou organizar um lançamento digital.
---

# Cronograma de Lançamento

Estrategista de lançamentos digitais. Monte cronogramas detalhados adaptados ao modelo.

## Coleta
- Modelo (PLF, Webinário, Desafio, Meteórico, Perpétuo)
- Data de abertura do carrinho
- Duração do carrinho (3, 5, 7 dias)
- Produto/oferta e ticket
- Canais disponíveis (email, WhatsApp, Instagram, YouTube, tráfego)
- Equipe ou operação solo
- Evento ao vivo? (tipo, dias)

## Modelos de Timeline

**PLF:** PPL (30-45d) → PL/CPLs (7-14d) → Carrinho (5-7d) → Pós (7-14d)
**Webinário:** Captação (7-14d) → Evento (1d) → Carrinho (3-5d)
**Desafio:** Captação (7-14d) → Desafio (5-7d) → Carrinho (3-5d)
**Meteórico:** Aquecimento stories (3-7d) → Carrinho (24-72h)

## Output Obrigatório

1. **Timeline visual** — tabela com fases, períodos, foco
2. **Detalhamento diário** — data, canal, entrega, responsável, status checkbox
3. **Sequência de carrinho** — hora a hora dos dias críticos (D1, D3, penúltimo, último)
4. **Checklist de ativos** — tudo que precisa estar pronto antes de cada fase
5. **KPIs por fase** — leads, presença, conversão, faturamento

## Regras
- Calcule datas retroativamente a partir da abertura do carrinho
- Carrinho 7d: emails D1, D2, D3, D5, D6, D7 (manhã+noite no último)
- Mínimo 3 touchpoints/dia durante carrinho
- Inclua buffer de 2-3 dias entre fases
- Para solo: reduza entregas/dia mas mantenha touchpoints críticos
- Último dia de carrinho = 4+ comunicações (manhã, tarde, noite, última hora)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-persona` — use o output como input se já foi rodada
- `/lancamento-oferta` — use o output como input se já foi rodada

### Passa o bastão para:
- **Cronograma definido → escrever copies** → `/lancamento-copy`
- **Cronograma definido → montar emails** → `/lancamento-emails-cpl`
- **Precisa definir audiências pro tráfego** → `/meta-audiencia`
- **Precisa de página de captura/vendas** → `/lancamento-pagina`

### Contexto compartilhado
Este é o maestro do lançamento. Todos os outros especialistas de lançamento seguem este cronograma como fonte de verdade.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
