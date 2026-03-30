---
name: negocios-pitch
description: Cria pitch decks e apresentações de negócio para investidores, clientes e parceiros. Use quando o usuário pedir pitch deck, apresentação para investidor, deck de vendas, one-pager, ou apresentação institucional de negócio.
---

# Pitch Deck

Crie apresentações que comunicam valor e convencem stakeholders.

## Estruturas por Objetivo

### Pitch para Investidor (10-12 slides)
1. **Capa** — Logo + tagline + rodada
2. **Problema** — Dor do mercado com dados
3. **Solução** — Como você resolve
4. **Produto** — Demo/screenshots
5. **Modelo de Negócio** — Como gera receita
6. **Tração** — Métricas reais (MRR, crescimento, clientes)
7. **Mercado** — TAM/SAM/SOM
8. **Concorrência** — Posicionamento (matrix 2x2)
9. **Time** — Fundadores + experiência relevante
10. **Financeiro** — Projeções 3-5 anos
11. **Ask** — Quanto, para quê, milestones
12. **Contato** — CTA

### Pitch Comercial/Vendas (6-8 slides)
1. Capa
2. Problema do cliente
3. Solução e diferenciais
4. Como funciona
5. Resultados/cases
6. Planos e preços
7. Próximos passos

### One-Pager (1 página)
- Problema → Solução → Tração → Modelo → Time → Ask

## Output

```markdown
# 🎤 Pitch Deck — [Empresa]
**Objetivo:** [investidor/cliente/parceiro]
**Rodada/Contexto:** [X]

## Slide 1: Capa
**Título:** [Nome da Empresa]
**Subtítulo:** [Tagline — 1 frase que resume a proposta de valor]
[Logo + visual sugerido]

## Slide 2: Problema
**Headline:** [frase impactante sobre o problema]
**Dados:**
- [dado 1 que dimensiona o problema]
- [dado 2]
- [dado 3]
**Visual sugerido:** [ícone/ilustração]

## Slide 3: Solução
**Headline:** [como resolvem]
**Bullets:**
- [benefício 1]
- [benefício 2]
- [benefício 3]

[Continuar para cada slide...]

## Notas de Apresentação
- **Slide 1:** [talking points — 30s]
- **Slide 2:** [talking points — 60s]
[...]

## Timing Total: [X minutos]
```

## Regras
- 1 ideia por slide — se precisa de 2 ideias, são 2 slides
- Dados > opinião. Sempre que possível, use números
- Máximo 20 palavras por slide (o apresentador completa com a fala)
- Para investidor: tração real > projeção otimista
- TAM/SAM/SOM: use fontes confiáveis, não números inventados
- Concorrência: nunca diga "não temos concorrentes" — sempre tem
- Ask claro: quanto precisa, para que vai usar, que milestones vai atingir
- Design: menos é mais. Fundos limpos, tipografia grande, contraste alto
- Deck para enviar por email ≠ deck para apresentar (o enviado precisa de mais texto)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-forecasting` — use o output como input se já foi rodada
- `/negocios-diagnostico` — use o output como input se já foi rodada

### Passa o bastão para:
- **Deck pronto → design** → `/design-apresentacao`

### Contexto compartilhado
Tração real vem dos KPIs. Projeções vêm do forecast. Mercado vem da análise de concorrentes.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
