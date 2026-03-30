---
name: instagram-roteiro
description: Escreve roteiros para Reels e vídeos do Instagram com estrutura de hook, desenvolvimento e CTA. Use quando o usuário pedir roteiro de reels, script de vídeo para Instagram, estrutura de vídeo curto, roteiro de conteúdo em vídeo, ou texto para gravar reels.
---

# Roteiro de Reels/Vídeos Instagram

Crie roteiros com estrutura que maximiza retenção e engajamento.

## Framework Padrão: HDPM
1. **Hook (0-3s)** — Para o scroll. Frase ou ação impactante.
2. **Desenvolvimento (3-30s)** — Entregue o conteúdo/valor prometido.
3. **Plot Twist (30-45s)** — Elemento surpresa, dado inesperado, virada.
4. **Moral/CTA (45-60s)** — Conclusão + chamada para ação.

## Tipos de Hook

- **Imperativo:** "Para de fazer [X] agora"
- **Revelação:** "Olha o que descobri sobre [X]"
- **Polêmica:** "[Afirmação controversa do nicho]"
- **Resultado:** "Fiz [X] e aconteceu [Y]"
- **Pergunta:** "Você sabia que [dado surpreendente]?"
- **Pattern interrupt:** Ação visual inesperada + frase curta

## Output

```markdown
# 🎬 Roteiro Reels — [Tema]

**Duração alvo:** [15s / 30s / 60s / 90s]
**Formato:** [talking head / b-roll + narração / trend + conteúdo]

---

## HOOK (0-3s)
**Texto na tela:** "[frase de impacto curta]"
**Fala:** "[o que dizer]"
**Visual:** [descrição do que aparece/acontece]

## DESENVOLVIMENTO (3-Xs)
**Ponto 1:** "[frase]"
**Visual:** [descrição]

**Ponto 2:** "[frase]"
**Visual:** [descrição]

**Ponto 3:** "[frase]"
**Visual:** [descrição]

## PLOT TWIST (Xs-Ys)
**Fala:** "[virada inesperada]"
**Visual:** [transição ou mudança de cenário]

## CTA (Ys-final)
**Fala:** "[moral + CTA]"
**Texto na tela:** "[CTA escrito — salva/compartilha/comenta]"

---

**Áudio sugerido:** [trending audio ou original]
**Hashtags:** [5-10]
**Legenda:** [legenda curta para o post]
**Melhor horário:** [sugestão]
```

## Regras
- Hook de 3 segundos é inegociável — se não prender, o resto não importa
- Textos na tela devem ser legíveis em 2s (máx 8-10 palavras)
- Reels de 30-60s têm melhor distribuição no algoritmo atual
- Sempre inclua texto na tela + fala (muitos assistem no mudo)
- Plot twist diferencia conteúdo bom de conteúdo viral
- CTA "salva pra assistir de novo" > "segue" (salvamentos pesam mais no algoritmo)
- Para talking head: olhe para a câmera nos primeiros 3s
- Entregue 2-3 variações de roteiro para o mesmo tema quando possível

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/instagram-calendario` — use o output como input se já foi rodada
- `/marketing-persona` — use o output como input se já foi rodada

### Passa o bastão para:
- **Roteiro pronto → legenda** → `/instagram-copy`
- **Conteúdo longo → YouTube** → `/conteudo-script-video`

### Contexto compartilhado
Use o framework HDPM. Se a persona já existe, adapte o hook para a linguagem dela.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
