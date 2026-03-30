---
name: conteudo-script-video
description: Escreve scripts completos para vídeos de YouTube, webinários e vídeos de vendas (VSL). Use quando o usuário pedir roteiro de YouTube, script de vídeo longo, VSL, script de webinário, roteiro de aula, ou texto para vídeo de vendas.
---

# Script de Vídeo

Crie scripts profissionais para diferentes formatos de vídeo.

## Formatos

### YouTube (8-15 min)
**Estrutura:** Hook (30s) → Intro/Promessa (30s) → Conteúdo (5-12 min) → CTA (30s)
- Hook: abra com o resultado ou a polêmica, nunca com "Fala galera"
- Retenção: inclua "pattern interrupts" a cada 2-3 minutos
- End screen: CTA para próximo vídeo + inscrição nos últimos 20s

### VSL — Video Sales Letter (15-45 min)
**Estrutura:** Hook → Problema → Agitação → Credenciais → Solução → Oferta → CTA
- Primeira versão: 20-30 minutos
- Cada seção tem um objetivo emocional claro
- Nunca revele o preço antes de construir valor suficiente

### Webinário (60-90 min)
**Estrutura:** Boas-vindas (5min) → Conteúdo de valor (30-40min) → Transição (5min) → Oferta (15-20min) → Q&A (10-15min)
- Conteúdo deve gerar "aha moments" sem entregar o "como" completo
- Transição entre conteúdo e oferta deve ser natural (não abrupta)

## Output

```markdown
# 🎥 Script — [Título do Vídeo]
**Formato:** [YouTube / VSL / Webinário]
**Duração alvo:** [X minutos]
**Público:** [descrição]

---

## HOOK (0:00 - 0:30)
[Texto exato para falar]

**Nota de produção:** [instrução de câmera/edição]

## [SEÇÃO 1] (0:30 - X:XX)
### Ponto principal
[Texto]

### Sub-ponto
[Texto]

**Pattern interrupt:** [ação/visual/pergunta para manter atenção]

## [SEÇÃO 2] (X:XX - Y:YY)
[mesma estrutura]

## CTA (Y:YY - final)
[Texto exato do CTA]

---

**Thumbnail sugerido:** [descrição da thumbnail]
**Título SEO:** [título otimizado — máx 60 chars]
**Descrição YouTube:** [primeiras 2 linhas com keyword]
**Tags:** [10-15 tags relevantes]
```

## Regras
- Scripts devem ser escritos para serem FALADOS (linguagem oral, não escrita)
- Marque pausas, ênfases e mudanças de tom no script
- Para YouTube: os primeiros 30s determinam se o vídeo será assistido — investir ali
- Para VSL: cada seção deve aumentar a tensão emocional progressivamente
- Inclua timestamps para facilitar gravação e edição
- Nunca escreva mais de 2 minutos de conteúdo sem uma mudança de ritmo

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/instagram-roteiro` — use o output como input se já foi rodada
- `/marketing-persona` — use o output como input se já foi rodada

### Passa o bastão para:
- **Vídeo é sobre o produto → VSL** → `/lancamento-pagina`
- **Vídeo é conteúdo → distribuir** → `/instagram-copy`

### Contexto compartilhado
Para YouTube, use os dados de pauta SEO para otimizar título e descrição.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
