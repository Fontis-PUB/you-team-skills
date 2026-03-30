---
name: instagram-hashtag
description: Pesquisa e estrutura estratégias de hashtags para Instagram com mix de volume, nicho e branded. Use quando o usuário pedir hashtags, pesquisa de hashtags, estratégia de hashtags, tags para post, ou otimização de hashtags para Instagram.
---

# Estratégia de Hashtags Instagram

Estruture sets de hashtags otimizados para alcance e descoberta.

## Framework de Mix

Para cada post, use 15-20 hashtags distribuídas:
- **Alta competição (500K+):** 3-4 tags — para alcance potencial
- **Média competição (50-500K):** 5-7 tags — melhor custo-benefício
- **Nicho (<50K):** 5-7 tags — maior chance de rankear no top
- **Branded (1-2):** hashtag da marca/campanha

## Output

```markdown
# #️⃣ Estratégia de Hashtags — [Perfil/Nicho]

## Set A — [Tipo de Post: Educativo]
**Alta:** #[tag] (Xm) | #[tag] (Xm) | #[tag] (Xm)
**Média:** #[tag] (Xk) | #[tag] (Xk) | #[tag] (Xk) | #[tag] (Xk)
**Nicho:** #[tag] (Xk) | #[tag] (Xk) | #[tag] (Xk) | #[tag] (Xk)
**Branded:** #[tag]
**Total:** [15-20]

## Set B — [Tipo de Post: Engajamento]
[mesma estrutura]

## Set C — [Tipo de Post: Vendas]
[mesma estrutura]

## Regras de Uso
- Alterne entre sets (nunca use o mesmo set 2x seguidas — shadow ban risk)
- Coloque hashtags no primeiro comentário (não na legenda)
- Revise mensalmente — hashtags saturam
```

## Regras
- Pesquise hashtags reais do nicho em português BR
- Evite hashtags banidas pelo Instagram (#adulting, #beautyblogger etc — muda frequentemente)
- Hashtags em inglês só se o público for internacional
- Para contas pequenas (<10K): foque 70% em nicho, 30% em média
- Para contas maiores (>50K): pode usar mais alta competição
- Nunca use hashtags genéricas sem relação (#love #instagood) — prejudica a categorização
- Crie 4-5 sets diferentes e alterne

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/instagram-copy` — use o output como input se já foi rodada
- `/instagram-calendario` — use o output como input se já foi rodada

### Contexto compartilhado
Hashtags devem ser coerentes com o pilar de conteúdo definido no calendário.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
