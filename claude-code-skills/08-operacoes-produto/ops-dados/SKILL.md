---
name: ops-dados
description: Analisa dados de negócio — extrai insights de planilhas, CSVs e bancos de dados, cria dashboards e relatórios analíticos. Use quando o usuário pedir análise de dados, dashboard, relatório analítico, insights de planilha, visualização de dados, SQL, ou qualquer trabalho com dados do negócio.
---

# Análise de Dados

Transforme dados brutos em insights acionáveis para decisão.

## Processo de Análise

### 1. Entender o Contexto
- Qual pergunta de negócio estamos respondendo?
- Que decisão será tomada com base nesta análise?
- Quem vai consumir o resultado?

### 2. Coletar e Limpar
- Fonte dos dados (planilha, CSV, banco, API)
- Qualidade: valores faltantes, duplicatas, outliers
- Período de análise
- Granularidade (diário, semanal, mensal)

### 3. Analisar
- Métricas descritivas (média, mediana, distribuição)
- Tendências (crescimento, sazonalidade, anomalias)
- Segmentação (por canal, produto, região, cohort)
- Correlações (X influencia Y?)

### 4. Comunicar
- Insight principal em 1 frase
- Visualização adequada ao tipo de dado
- Recomendação de ação

## Tipos de Análise

### Análise de Cohort
Acompanhe grupos de clientes ao longo do tempo.
```
| Cohort | M0 | M1 | M2 | M3 | M6 | M12 |
|--------|-----|-----|-----|-----|-----|-----|
| Jan/25 | 100% | 85% | 72% | 65% | 48% | 32% |
| Fev/25 | 100% | 82% | 70% | ... | | |
```

### Análise de Funil
```
| Etapa | Volume | Conversão | Drop-off |
|-------|--------|-----------|----------|
| Visitantes | 10.000 | — | — |
| Leads | 500 | 5% | 95% |
| MQLs | 150 | 30% | 70% |
| SQLs | 50 | 33% | 67% |
| Clientes | 15 | 30% | 70% |
```

### Análise RFM (Recency, Frequency, Monetary)
Segmente clientes por comportamento de compra.

### Análise de Pareto (80/20)
Identifique os 20% que geram 80% do resultado.

## Output

```markdown
# 📊 Análise — [Tema]
**Período:** [X]
**Fonte:** [X]
**Pergunta de negócio:** [X]

## TL;DR
[Insight principal em 1-2 frases + recomendação]

## Dados Analisados
- Registros: [X]
- Período: [X]
- Segmentos: [X]
- Qualidade: [X% completo, X outliers removidos]

## Findings

### Finding 1: [título do insight]
[Descrição com dados]
[Visualização: tabela ou descrição de gráfico]
**Implicação:** [o que isso significa para o negócio]

### Finding 2: [título do insight]
[mesma estrutura]

## Recomendações
1. **[Ação]** — baseada em [finding X] — impacto estimado: [X]
2. **[Ação]** — baseada em [finding Y] — impacto estimado: [X]

## Limitações
- [O que os dados NÃO mostram]
- [Vieses possíveis]
- [Dados que faltam]

## Próximos Passos
- [Análise mais profunda necessária em X]
- [Dados adicionais a coletar]
```

## Regras
- Sempre comece com a pergunta de negócio (não com os dados)
- Dados sem contexto são inúteis — sempre conecte com decisão de negócio
- Declare limitações (dados incompletos, período curto, viés de seleção)
- Gráficos: o tipo certo para o dado certo (tendência=linha, comparação=barra, proporção=pizza, distribuição=histograma)
- Correlação ≠ causalidade — seja preciso na linguagem
- Para quem não é técnico: insight + recomendação > metodologia + detalhes técnicos
- Se os dados dizem algo contraintuitivo, investigue antes de reportar

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-kpis` — use o output como input se já foi rodada
- `/ops-cs` — use o output como input se já foi rodada
- `/lancamento-metricas` — use o output como input se já foi rodada

### Passa o bastão para:
- **Insights → ação de marketing** → `/marketing-campanha`
- **Insights → ajustar funil** → `/marketing-funil`
- **Insights → forecast** → `/negocios-forecasting`

### Contexto compartilhado
Análises devem responder perguntas de negócio, não gerar relatórios bonitos.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
