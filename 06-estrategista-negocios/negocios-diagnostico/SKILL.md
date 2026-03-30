---
name: negocios-diagnostico
description: Realiza diagnósticos empresariais completos — análise SWOT, health check de áreas, identificação de gargalos e plano de ação. Use quando o usuário pedir diagnóstico de negócio, análise SWOT, avaliação empresarial, health check, ou quiser entender onde estão os problemas e oportunidades da empresa.
---

# Diagnóstico Empresarial

Realize diagnósticos estruturados que identificam gargalos e oportunidades.

## Framework de Diagnóstico

### 1. Visão Geral
- Modelo de negócio (como gera receita)
- Estágio (validação, tração, escala, maturidade)
- Faturamento e margem
- Equipe e estrutura
- Tempo de operação

### 2. Análise por Área (Health Score A-F)

**Comercial/Vendas**
- Pipeline e conversão
- Ticket médio e recorrência
- CAC e LTV
- Processo de vendas documentado?

**Marketing**
- Canais de aquisição e performance
- Presença digital e autoridade
- Funil estruturado?
- Conteúdo e frequência

**Operações/Entrega**
- Qualidade do produto/serviço
- Tempo de entrega
- Satisfação do cliente (NPS)
- Processos documentados?

**Financeiro**
- Margem de contribuição
- Fluxo de caixa
- Ponto de equilíbrio
- Custos fixos vs variáveis

**Pessoas**
- Organograma
- Gargalos de pessoa
- Cultura e retenção
- Dependência do fundador

### 3. SWOT

| | Positivo | Negativo |
|---|---------|---------|
| **Interno** | Forças | Fraquezas |
| **Externo** | Oportunidades | Ameaças |

## Output

```markdown
# 🏢 Diagnóstico Empresarial — [Empresa]
**Data:** [dd/mm/yyyy]
**Estágio:** [validação/tração/escala]
**Faturamento:** R$ [X]/mês

## Health Score por Área

| Área | Score | Principais Issues |
|------|-------|-------------------|
| Comercial | [A-F] | [resumo] |
| Marketing | [A-F] | [resumo] |
| Operações | [A-F] | [resumo] |
| Financeiro | [A-F] | [resumo] |
| Pessoas | [A-F] | [resumo] |

## SWOT
[Matriz preenchida]

## Top 3 Gargalos (por impacto)
1. **[Gargalo]** — Impacto: R$ X/mês | Área: [X]
2. **[Gargalo]** — Impacto: R$ X/mês | Área: [X]
3. **[Gargalo]** — Impacto: R$ X/mês | Área: [X]

## Top 3 Oportunidades (por viabilidade)
1. **[Oportunidade]** — Potencial: R$ X/mês | Esforço: [baixo/médio/alto]
2. **[Oportunidade]** — Potencial: R$ X/mês | Esforço: [baixo/médio/alto]
3. **[Oportunidade]** — Potencial: R$ X/mês | Esforço: [baixo/médio/alto]

## Plano de Ação — 90 Dias

| Prioridade | Ação | Área | Responsável | Prazo | Impacto |
|-----------|------|------|-------------|-------|---------|
| 1 | [X] | [X] | [X] | [X] | [X] |
| 2 | [X] | [X] | [X] | [X] | [X] |
| 3 | [X] | [X] | [X] | [X] | [X] |
```

## Regras
- Diagnóstico sem dados é opinião — peça números sempre que possível
- Priorize gargalos por impacto financeiro (R$/mês perdido ou potencial)
- Score A-F: A=excelente, B=bom, C=adequado, D=precisa melhorar, F=crítico
- Plano de 90 dias com no máximo 5 ações (foco > volume)
- Identifique a "one thing" — a alavanca que mais impacta o negócio agora
- Dependência do fundador é quase sempre um gargalo — sempre avalie

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Passa o bastão para:
- **Área comercial fraca** → `/marketing-funil`
- **Área marketing fraca** → `/marketing-persona`
- **Área financeira fraca** → `/ops-financeiro`
- **Área operacional fraca** → `/negocios-processos`
- **Todas as áreas → plano integrado** → `/team-orchestrator`

### Contexto compartilhado
Este é o ponto de entrada do time. O diagnóstico aciona todas as outras áreas conforme o score.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
