---
name: ops-produto
description: Gerencia produto digital — roadmap, priorização, user stories, sprints e métricas de produto. Use quando o usuário pedir roadmap de produto, backlog, user stories, priorização de features, sprint planning, PRD, ou gestão de produto digital.
---

# Gestão de Produto

Estruture roadmap, backlog e processos de produto.

## Entregáveis

### Roadmap

```markdown
## Roadmap — [Produto] — [Trimestre/Ano]

### Visão
[Para onde o produto está indo em 1 frase]

### Temas do Trimestre
1. **[Tema 1]** — [por que é prioridade agora]
2. **[Tema 2]** — [por que é prioridade agora]
3. **[Tema 3]** — [por que é prioridade agora]

### Timeline

| Mês | Tema | Entregas | Impacto Esperado |
|-----|------|----------|-----------------|
| M1 | [X] | [features] | [métrica] |
| M2 | [X] | [features] | [métrica] |
| M3 | [X] | [features] | [métrica] |

### Icebox (não agora, mas no radar)
- [feature/ideia] — [motivo de estar no icebox]
```

### PRD (Product Requirements Document)

```markdown
## PRD — [Feature]
**Autor:** [PM]
**Status:** [draft/review/approved]
**Sprint target:** [X]

### Problema
[Que problema do usuário estamos resolvendo?]
[Dados/evidências que suportam]

### Solução Proposta
[Descrição da feature]

### User Stories
- Como [persona], quero [ação], para [benefício]
- Como [persona], quero [ação], para [benefício]

### Critérios de Aceite
- [ ] [critério 1 — verificável]
- [ ] [critério 2 — verificável]
- [ ] [critério 3 — verificável]

### Escopo
**Inclui:** [o que faz parte desta entrega]
**Não inclui:** [o que fica de fora]

### Métricas de Sucesso
| Métrica | Baseline | Meta | Prazo |
|---------|----------|------|-------|
| [X] | [atual] | [alvo] | [data] |

### Riscos e Dependências
| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| [X] | Alta/Média/Baixa | [X] | [X] |
```

### Framework de Priorização (RICE)

| Feature | Reach | Impact | Confidence | Effort | RICE Score |
|---------|-------|--------|-----------|--------|------------|
| [feat 1] | [users/mês] | [1-3] | [%] | [person-weeks] | [score] |

**RICE = (Reach × Impact × Confidence) / Effort**

## Regras
- Roadmap é compromisso de direção, não de datas específicas
- User stories no formato: Como [quem], quero [o quê], para [por quê]
- Critérios de aceite devem ser testáveis (sim/não)
- Priorize por impacto no usuário E no negócio (não por facilidade)
- "Não inclui" no PRD é tão importante quanto "Inclui" (evita scope creep)
- Métricas de sucesso definidas ANTES do desenvolvimento, não depois
- Icebox ≠ lixo. Revise mensalmente — contexto muda.

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-diagnostico` — use o output como input se já foi rodada
- `/ops-cs` — use o output como input se já foi rodada

### Passa o bastão para:
- **PRD pronto → design** → `/design-ui-ux`
- **Feature request do CS** → `/ops-cs`

### Contexto compartilhado
Feedback de clientes via CS alimenta o backlog. Priorize por RICE.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
