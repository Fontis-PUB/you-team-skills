---
name: marketing-concorrentes
description: Pesquisa e analisa concorrentes — posicionamento, preços, canais, pontos fortes e fracos, oportunidades de diferenciação. Use quando o usuário pedir análise de concorrência, benchmark competitivo, pesquisa de mercado, mapeamento de concorrentes, ou comparativo com competidores.
---

# Análise de Concorrentes

Mapeie o cenário competitivo e identifique oportunidades de diferenciação.

## Dimensões de Análise

1. **Produto/Serviço** — o que oferecem, features, qualidade
2. **Preço** — faixas, modelos (assinatura, único, freemium)
3. **Comunicação** — tom, canais, frequência, tipo de conteúdo
4. **Posicionamento** — como se posicionam, para quem falam
5. **Distribuição** — onde vendem, canais de aquisição
6. **Prova Social** — reviews, cases, presença de marca
7. **Pontos Fracos** — reclamações, gaps identificados

## Output

```markdown
# 🔍 Análise Competitiva — [Seu Negócio]

## Mapa de Concorrentes

| Concorrente | Tipo | Força | Fraqueza | Ameaça |
|-------------|------|-------|----------|--------|
| [nome] | Direto | [X] | [X] | Alta/Média/Baixa |
| [nome] | Direto | [X] | [X] | Alta/Média/Baixa |
| [nome] | Indireto | [X] | [X] | Alta/Média/Baixa |

## Análise Detalhada

### [Concorrente 1]
- **O que fazem:** [descrição]
- **Público-alvo:** [quem atendem]
- **Preço:** R$ [faixa] / [modelo]
- **Canais principais:** [Instagram, Google, etc]
- **Pontos fortes:** [lista]
- **Pontos fracos:** [lista — baseado em reviews, Reclame Aqui, etc]
- **O que podemos aprender:** [insight acionável]

[Repetir para cada concorrente]

## Comparativo

| Dimensão | Você | Conc. A | Conc. B | Conc. C |
|----------|------|---------|---------|---------|
| Preço | R$X | R$X | R$X | R$X |
| [feature 1] | ✅/❌ | ✅/❌ | ✅/❌ | ✅/❌ |
| [feature 2] | ✅/❌ | ✅/❌ | ✅/❌ | ✅/❌ |
| Avaliação | X/5 | X/5 | X/5 | X/5 |

## Oportunidades de Diferenciação
1. **[Oportunidade]** — [por que é viável + como capturar]
2. **[Oportunidade]** — [por que é viável + como capturar]
3. **[Oportunidade]** — [por que é viável + como capturar]

## Ameaças para Monitorar
1. [ameaça + trigger de ação]
2. [ameaça + trigger de ação]
```

## Regras
- Analise mínimo 3 concorrentes diretos + 2 indiretos
- Concorrente indireto = resolve o mesmo problema de forma diferente
- Reclame Aqui e reviews do Google são OURO para encontrar fraquezas
- Não copie — identifique gaps para diferenciação
- Atualize a cada trimestre (mercado muda rápido)
- Inclua concorrentes aspiracionais (quem você quer superar em 2 anos)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-diagnostico` — use o output como input se já foi rodada

### Passa o bastão para:
- **Gaps identificados → posicionamento** → `/negocios-precificacao`
- **Oportunidades de conteúdo** → `/conteudo-pauta-seo`
- **Diferenciação → copy** → `/meta-copy-criativo`

### Contexto compartilhado
A análise competitiva informa precificação, posicionamento e comunicação.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
