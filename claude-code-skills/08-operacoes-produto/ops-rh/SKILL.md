---
name: ops-rh
description: Gerencia processos de RH — descrições de vaga, onboarding, avaliação de performance, PDI e cultura organizacional. Use quando o usuário pedir para criar vaga, job description, processo seletivo, onboarding de funcionário, avaliação de desempenho, PDI, ou qualquer processo de gestão de pessoas.
---

# Operações de RH

Estruture processos de gestão de pessoas de forma escalável.

## Entregáveis

### Job Description
```markdown
## [Cargo] — [Empresa]
**Modelo:** [CLT/PJ/Estágio]
**Local:** [Remoto/Presencial/Híbrido — cidade]
**Faixa salarial:** R$ [X] - R$ [Y]

### Sobre a empresa
[2-3 linhas]

### Sobre a posição
[O que a pessoa vai fazer e por que a posição existe]

### Responsabilidades
- [Responsabilidade 1 — com verbo de ação]
- [Responsabilidade 2]
- [Responsabilidade 3]

### Requisitos
**Obrigatórios:**
- [Hard skill / experiência / formação]

**Desejáveis:**
- [Diferencial]

### Benefícios
- [Benefício 1]
- [Benefício 2]

### Como se candidatar
[Instruções claras]
```

### Onboarding (30-60-90)
```markdown
## Onboarding — [Cargo]

### Pré-Day 1
- [ ] Acessos criados (email, Slack, ferramentas)
- [ ] Equipamento preparado
- [ ] Buddy designado
- [ ] Agenda da primeira semana enviada

### Semana 1 (Day 1-5)
- [ ] Tour pela empresa/equipe
- [ ] Cultura e valores
- [ ] Ferramentas e processos
- [ ] Primeira tarefa guiada

### 30 dias — Aprender
- Meta: [entender o contexto e processos]
- Entregas esperadas: [lista]
- Check-in: [data]

### 60 dias — Contribuir
- Meta: [começar a entregar com autonomia]
- Entregas esperadas: [lista]
- Check-in: [data]

### 90 dias — Performar
- Meta: [operar com independência total]
- Entregas esperadas: [lista]
- Avaliação formal: [data]
```

### Avaliação de Performance
```markdown
## Avaliação — [Nome] — [Período]

### Resultados vs Metas
| Meta | Resultado | Score |
|------|-----------|-------|
| [meta definida] | [entrega real] | [1-5] |

### Competências
| Competência | Auto | Gestor | Pares |
|-------------|------|--------|-------|
| [competência 1] | X/5 | X/5 | X/5 |

### Feedback
**Pontos fortes:** [lista]
**Áreas de desenvolvimento:** [lista]
**Feedback do gestor:** [texto]

### PDI (Plano de Desenvolvimento Individual)
| Área | Ação | Prazo | Suporte |
|------|------|-------|---------|
| [skill] | [ação concreta] | [data] | [recurso/mentoria] |
```

## Regras
- Job descriptions: foque no que a pessoa FAZ, não em requisitos impossíveis
- Onboarding: os primeiros 90 dias definem retenção — investir tempo aqui poupa dinheiro depois
- Avaliação: feedback construtivo (específico + orientado para ação + com suporte)
- PDI: máximo 3 áreas de foco por trimestre
- Para startups: processos simples > processos perfeitos (documente o mínimo viável)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-diagnostico` — use o output como input se já foi rodada

### Passa o bastão para:
- **Vaga publicada → funil de candidatos** → `/comercial-crm`
- **Novo funcionário → onboarding** → `/ops-documentacao`

### Contexto compartilhado
Contratações devem endereçar os gargalos identificados no diagnóstico.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
