---
name: instagram-calendario
description: Planeja calendários editoriais para Instagram com mix de formatos, pilares de conteúdo e distribuição estratégica. Use quando o usuário pedir calendário de conteúdo, planejamento de posts, grade de publicações, cronograma de Instagram, editorial mensal, ou organização de conteúdo semanal/mensal para Instagram.
---

# Calendário Editorial Instagram

Planeje calendários de conteúdo equilibrados entre atração, engajamento, autoridade e conversão.

## Coleta
- Nicho/segmento
- Pilares de conteúdo (ou ajude a definir)
- Frequência de posts desejada (3-7x/semana)
- Objetivo principal (crescimento, engajamento, vendas)
- Formatos preferidos (reels, carrossel, estático, stories)
- Datas comemorativas/lançamentos no período

## Framework AEAC

Distribua os posts no mês:
- **A**tração (30%) — reels virais, trends, conteúdo de descoberta
- **E**ngajamento (25%) — enquetes, caixinhas, debates, memes do nicho
- **A**utoridade (25%) — carrosséis educativos, cases, bastidores técnicos
- **C**onversão (20%) — CTA direto, oferta, prova social, depoimentos

## Output

```markdown
# 📅 Calendário Instagram — [Mês/Ano]
**Perfil:** @[handle]
**Frequência:** [X] posts/semana + stories diários

## Pilares de Conteúdo
1. [Pilar 1] — [descrição curta]
2. [Pilar 2] — [descrição curta]
3. [Pilar 3] — [descrição curta]
4. [Pilar 4] — [descrição curta]

## Semana 1 — [dd/mm a dd/mm]

| Dia | Formato | Pilar | Tipo AEAC | Tema | Status |
|-----|---------|-------|-----------|------|--------|
| Seg | Reels | Pilar 1 | Atração | [tema] | ⬜ |
| Ter | — | — | Stories only | [tema stories] | ⬜ |
| Qua | Carrossel | Pilar 2 | Autoridade | [tema] | ⬜ |
| Qui | — | — | Stories only | [tema stories] | ⬜ |
| Sex | Reels | Pilar 3 | Engajamento | [tema] | ⬜ |
| Sáb | Estático | Pilar 1 | Conversão | [tema] | ⬜ |
| Dom | — | — | Descanso/stories | — | ⬜ |

[Repetir para semanas 2, 3, 4]

## Datas Estratégicas do Mês
- [dd/mm] — [evento/data comemorativa] → [tipo de post planejado]

## Rotina de Stories (Diária)
- Manhã: [tipo — bastidores, rotina, check-in]
- Tarde: [tipo — conteúdo, enquete, dica]
- Noite: [tipo — reflexão, CTA, caixinha]

## Métricas para Acompanhar
- Alcance por post (meta: [X])
- Taxa de salvamento (meta: >2%)
- Crescimento de seguidores (meta: +[X]/semana)
- Cliques no link da bio (meta: [X]/semana)
```

## Regras
- Nunca publique 2 posts de conversão seguidos — intercale com valor
- Reels: mínimo 3x/semana para crescimento
- Carrossel educativo: 1-2x/semana para autoridade
- Sempre inclua pelo menos 1 post de storytelling/pessoal por semana
- Stories: mínimo 5/dia para manter relevância no algoritmo
- Domingo é dia de menor engajamento — ideal para stories leves ou descanso
- Adapte horários ao analytics do perfil (se disponível)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-persona` — use o output como input se já foi rodada
- `/marketing-concorrentes` — use o output como input se já foi rodada

### Passa o bastão para:
- **Cada post precisa de legenda** → `/instagram-copy`
- **Posts de vídeo precisam de roteiro** → `/instagram-roteiro`
- **Todos precisam de hashtags** → `/instagram-hashtag`

### Contexto compartilhado
O calendário é o plano mestre do conteúdo. Copies, roteiros e hashtags devem seguir o que está aqui.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
