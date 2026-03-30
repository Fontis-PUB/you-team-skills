---
name: marketing-seo
description: Cria estratégias completas de SEO — auditoria técnica, on-page, off-page, content strategy e monitoramento. Use quando o usuário pedir estratégia de SEO, auditoria SEO, otimização para Google, rankeamento orgânico, link building, ou plano de SEO.
---

# Estratégia de SEO

Estruture planos de SEO completos com diagnóstico, priorização e roadmap.

## Pilares do SEO

### 1. SEO Técnico
- Velocidade (Core Web Vitals: LCP, FID, CLS)
- Mobile-friendly
- Indexação (sitemap, robots.txt, canonical)
- Estrutura de URLs
- Schema markup
- HTTPS
- Crawl errors

### 2. SEO On-Page
- Title tags e meta descriptions
- Heading hierarchy (H1-H6)
- Keyword placement e densidade
- Internal linking
- Image optimization (alt text, compressão)
- Content quality e E-E-A-T

### 3. SEO Off-Page
- Backlinks (qualidade > quantidade)
- Digital PR
- Guest posting
- Menções de marca
- Social signals

### 4. Conteúdo
- Topic clusters (pillar + cluster pages)
- Content gap analysis
- Atualização de conteúdo existente
- Featured snippet optimization

## Output

```markdown
# 🔎 Estratégia SEO — [Site]
**URL:** [domínio]
**Nicho:** [X]
**Objetivo:** [X posições top 10 em Y meses]

## Diagnóstico Rápido

| Área | Status | Prioridade |
|------|--------|-----------|
| Técnico | 🟢🟡🔴 | [alta/média/baixa] |
| On-Page | 🟢🟡🔴 | [alta/média/baixa] |
| Conteúdo | 🟢🟡🔴 | [alta/média/baixa] |
| Backlinks | 🟢🟡🔴 | [alta/média/baixa] |

## Quick Wins (Impacto em 30 dias)
1. [ação técnica ou on-page de implementação rápida]
2. [otimização de página existente]
3. [fix de erro técnico]

## Roadmap 6 Meses

**Mês 1-2:** Fundação técnica + on-page das top pages
**Mês 3-4:** Produção de conteúdo cluster + link building
**Mês 5-6:** Escala de conteúdo + PR + otimização contínua

## Topic Clusters

### Cluster 1: [tema pillar]
- **Pillar page:** [keyword] — [volume]
- **Cluster:** [keyword 1] — [volume]
- **Cluster:** [keyword 2] — [volume]
- **Cluster:** [keyword 3] — [volume]

## KPIs
- Tráfego orgânico: [meta mensal]
- Keywords top 10: [meta]
- Backlinks novos: [meta mensal]
- Conversões orgânicas: [meta]
```

## Regras
- SEO técnico vem ANTES de conteúdo (site lento = conteúdo desperdiçado)
- Foque em intent match: keyword certa + conteúdo certo + formato certo
- Quick wins primeiro: otimizar páginas já rankeando (pos 5-20) é mais rápido que criar novas
- Para sites novos: comece com long tail low competition, escale depois
- Backlinks de 1 domínio relevante > 100 backlinks de diretórios
- Atualize conteúdo existente a cada 6-12 meses (Google favorece freshness)
- E-E-A-T é crucial para YMYL (Your Money Your Life) — demonstre expertise e autoridade

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/conteudo-pauta-seo` — use o output como input se já foi rodada
- `/marketing-concorrentes` — use o output como input se já foi rodada

### Passa o bastão para:
- **Pautas prontas → blog** → `/conteudo-blog`
- **Keywords → Google Ads** → `/google-copy`

### Contexto compartilhado
SEO e Google Ads devem compartilhar inteligência de keywords.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
