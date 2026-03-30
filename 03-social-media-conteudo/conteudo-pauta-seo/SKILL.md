---
name: conteudo-pauta-seo
description: Pesquisa e estrutura pautas de conteúdo otimizadas para SEO — keywords, intenção de busca, estrutura de artigo e cluster de tópicos. Use quando o usuário pedir pesquisa de palavras-chave, pauta de blog SEO, planejamento de conteúdo para Google, estratégia de conteúdo orgânico, topic clusters, ou estrutura de artigo otimizado.
---

# Pauta de Conteúdo SEO

Estruture pautas completas com pesquisa de keywords, intenção de busca e arquitetura de conteúdo.

## Processo

1. Identifique o tema central e nicho
2. Pesquise keywords (principal + secundárias + long tail + perguntas)
3. Analise intenção de busca (informacional, navegacional, transacional, comercial)
4. Estruture o artigo com H1, H2, H3
5. Defina word count, internal links e CTAs

## Output

```markdown
# 📝 Pauta SEO — [Tema]

## Keyword Research

| Keyword | Volume | Dificuldade | Intenção | Prioridade |
|---------|--------|-------------|----------|-----------|
| [principal] | X/mês | Alta/Média/Baixa | Informacional | ⭐⭐⭐ |
| [secundária 1] | X/mês | Média | Informacional | ⭐⭐ |
| [long tail 1] | X/mês | Baixa | Transacional | ⭐⭐⭐ |
| [pergunta 1] | X/mês | Baixa | Informacional | ⭐⭐ |

## Análise da SERP
- **Tipo de conteúdo que rankeia:** [listicle / guia / tutorial / comparativo]
- **Word count médio do top 3:** [X palavras]
- **Featured snippet?** [Sim/Não — tipo: parágrafo/lista/tabela]
- **People Also Ask:** [lista de perguntas]

## Estrutura do Artigo

**H1:** [título otimizado com keyword principal — máx 60 chars]
**Meta description:** [155 chars com keyword + CTA]
**URL slug:** /[keyword-principal-separada-por-hifen]
**Word count alvo:** [X palavras]

### Outline

**Introdução** (100-150 palavras)
- Hook com a dor/pergunta do leitor
- Promessa do que o artigo entrega
- Keyword principal no primeiro parágrafo

**H2: [Subtítulo 1]**
- Keyword secundária: [X]
- Pontos a cobrir: [lista]
- [Sugestão: incluir imagem/tabela/exemplo]

**H2: [Subtítulo 2]**
[mesma estrutura]

**H2: [Subtítulo 3]**
[mesma estrutura]

**H2: FAQ / Perguntas Frequentes** (para featured snippet)
- H3: [pergunta 1]?
- H3: [pergunta 2]?
- H3: [pergunta 3]?

**Conclusão + CTA**
- Resumo dos pontos-chave
- CTA alinhado com intenção de busca

## SEO Checklist
- [ ] Keyword no H1, primeiro parágrafo, 1 H2, meta description, URL
- [ ] Densidade de keyword: 1-2% (natural, sem stuffing)
- [ ] Internal links: mínimo 3 para artigos relacionados
- [ ] External links: 2-3 para fontes de autoridade
- [ ] Imagens com alt text contendo keyword
- [ ] Schema markup sugerido: [FAQ / HowTo / Article]
```

## Regras
- Foque em keywords com volume real no Brasil (use variações em PT-BR)
- Long tail com intenção transacional > head terms informativos para negócios
- Sempre analise o que já rankeia antes de sugerir estrutura
- Para sites novos: priorize keywords de dificuldade baixa/média
- Cada artigo deve ter 1 keyword principal — nunca tente rankear para tudo
- Sugira topic clusters quando identificar oportunidade (pillar + clusters)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-persona` — use o output como input se já foi rodada
- `/marketing-concorrentes` — use o output como input se já foi rodada
- `/google-copy` — use o output como input se já foi rodada

### Passa o bastão para:
- **Pauta definida → escrever artigo** → `/conteudo-blog`
- **Keywords revelam oportunidades de ads** → `/google-copy`

### Contexto compartilhado
Keywords do Google Ads e do SEO devem conversar. Oportunidades orgânicas complementam o pago.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
