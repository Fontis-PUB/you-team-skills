---
name: conteudo-blog
description: Escreve artigos de blog completos, otimizados para SEO e com estrutura de conversão. Use quando o usuário pedir para escrever artigo, blog post, texto para blog, conteúdo de site, ou criar artigos longos otimizados para busca orgânica.
---

# Conteúdo de Blog

Escreva artigos completos que rankeiam no Google e convertem leitores em leads/clientes.

## Tipos de Artigo

- **Guia completo:** "Guia Definitivo de [X]" — 2.000-4.000 palavras
- **Listicle:** "X Melhores [Y] para [Z]" — 1.500-3.000 palavras
- **Tutorial:** "Como [fazer X] Passo a Passo" — 1.500-2.500 palavras
- **Comparativo:** "[X] vs [Y]: Qual Escolher?" — 1.500-2.500 palavras
- **Case study:** "Como [Empresa] Conseguiu [Resultado]" — 1.000-2.000 palavras

## Estrutura Padrão

1. **Headline** — Keyword + benefício + especificidade
2. **Introdução** — Hook → contexto → promessa → sumário do artigo
3. **Corpo** — H2s e H3s com keyword density natural
4. **Elementos visuais** — [indicar onde inserir imagens, tabelas, infográficos]
5. **FAQ** — Perguntas reais do "People Also Ask"
6. **Conclusão** — Resumo + CTA (newsletter, produto, próximo artigo)

## Regras de Escrita
- Parágrafos curtos (3-4 linhas máx)
- Uma ideia por parágrafo
- Frases ativas > passivas
- Dados e exemplos concretos > afirmações genéricas
- Subheadlines (H2/H3) a cada 200-300 palavras
- Transições suaves entre seções
- Tom: autoridade + acessibilidade (nem acadêmico nem coloquial demais)
- Incluir CTA contextual no meio do artigo (não só no final)
- Internal links naturais para outros conteúdos
- Nunca termine com "Conclusão" como H2 — use headline atrativa

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/conteudo-pauta-seo` — use o output como input se já foi rodada

### Passa o bastão para:
- **Artigo pronto → distribuir nas redes** → `/instagram-copy`
- **Artigo gera lead → funil** → `/marketing-funil`

### Contexto compartilhado
Siga a pauta SEO como brief. Inclua internal links para outros artigos já publicados.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
