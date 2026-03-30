---
name: lancamento-pagina
description: Estrutura páginas de captura e vendas para lançamentos digitais — wireframe, copy sections, layout e conversão. Use quando o usuário pedir para criar página de vendas, landing page de captura, página de lançamento, estrutura de sales page, wireframe de LP, ou copy de página para lançamento.
---

# Páginas de Lançamento

Estruture páginas de captura e vendas otimizadas para conversão.

## Página de Captura (LP de Leads)

### Estrutura (above the fold é tudo)
1. **Headline** — promessa + especificidade
2. **Subheadline** — contexto (para quem, quando, formato)
3. **Bullets** — 3-5 benefícios do evento/conteúdo gratuito
4. **Formulário** — nome + email (WhatsApp opcional)
5. **CTA** — texto de ação específico ("Quero minha vaga" > "Cadastrar")
6. **Prova social** — contador de inscritos ou depoimento rápido

### Benchmark: 25-45% de conversão

## Página de Vendas

### Estrutura Completa (seções em ordem)

1. **Hero** — Headline com promessa transformacional + subheadline + CTA
2. **Problema** — Descreva a dor do público (3-5 parágrafos)
3. **Agitação** — Consequências de não resolver
4. **Solução** — Apresente o produto como a ponte
5. **Autoridade** — Quem criou e por que essa pessoa é qualificada
6. **Método** — Como funciona (módulos, etapas, framework)
7. **Resultados** — Depoimentos, cases, números
8. **Oferta** — Stack de valor completo com ancoragem
9. **Preço** — Ancoragem → preço real → condições → CTA
10. **Garantia** — Badge + texto claro da garantia
11. **FAQ** — 5-8 perguntas (cada uma quebra uma objeção)
12. **CTA Final** — Recap + urgência + botão
13. **P.S.** — Resumo emocional da transformação

### Benchmark: 2-5% de conversão (da lista aquecida)

## Output

Entregue em formato markdown com:
- Cada seção identificada com número e nome
- Copy completo para cada seção
- Notas de design entre colchetes [imagem: depoimento em vídeo]
- Indicações de CTA ao longo da página (mínimo 3: hero, pós-oferta, final)

## Regras
- Mobile first — parágrafos curtos (máx 3 linhas), frases curtas
- CTA deve aparecer a cada 2-3 scrolls
- Depoimentos próximos ao preço (reduz fricção no momento da decisão)
- FAQ deve responder objeções reais, não perguntas genéricas
- Página de vendas de infoproduto: mínimo 2.000 palavras
- Página de captura: máximo 1 scroll (tudo above the fold no desktop)
- Nunca use pop-ups de saída em páginas de vendas de lançamento

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/lancamento-oferta` — use o output como input se já foi rodada
- `/lancamento-copy` — use o output como input se já foi rodada
- `/marketing-persona` — use o output como input se já foi rodada

### Passa o bastão para:
- **Página pronta → configurar tráfego** → `/meta-audiencia`
- **Precisa de design** → `/design-briefing`
- **Taxa de conversão baixa** → `/meta-analise-campanha`

### Contexto compartilhado
A página é o destino de todo o tráfego. O diagnóstico de campanha sempre deve cruzar com a performance da LP.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
