---
name: influencer
description: Estrutura estratégias de marketing de influência — seleção de influenciadores, briefing, contratos, métricas e gestão de campanhas. Use quando o usuário pedir estratégia de influenciadores, parceria com creators, briefing para influencer, campanha de influência, ou marketing com criadores de conteúdo.
---

# Marketing de Influência

Estruture campanhas de influência desde a seleção até a mensuração.

## Processo

### 1. Seleção de Influenciadores

| Tipo | Seguidores | Engagement | Custo | Melhor para |
|------|-----------|------------|-------|------------|
| Nano | 1-10K | 5-10% | R$100-500 | Nicho, prova social |
| Micro | 10-100K | 3-7% | R$500-5K | Conversão, authority |
| Mid | 100K-500K | 2-4% | R$5-30K | Alcance + conversão |
| Macro | 500K-1M | 1-3% | R$30-100K | Awareness |
| Mega | 1M+ | 0.5-2% | R$100K+ | Branding massivo |

### 2. Critérios de Avaliação
- Engagement rate REAL (não comprado)
- Alinhamento com a marca (valores, estética, público)
- Qualidade dos comentários (bots vs. pessoas reais)
- Histórico de collabs anteriores
- Audiência brasileira real (não inflada com internacionais)

## Output

```markdown
# 🤝 Campanha de Influência — [Produto/Marca]

## Estratégia
- **Objetivo:** [awareness/conversão/UGC]
- **Budget:** R$ [X]
- **Período:** [dd/mm — dd/mm]
- **Formato:** [publipost/stories/reels/unboxing/review]

## Perfil de Influenciador Ideal
- Nicho: [X]
- Seguidores: [faixa]
- Engagement mínimo: [X%]
- Localização: [X]
- Tom: [X]

## Shortlist

| Influenciador | Seguidores | Eng. Rate | Custo Est. | Fit | Prioridade |
|---------------|-----------|-----------|-----------|-----|-----------|
| @[handle] | Xk | X% | R$ X | Alto | 1 |
| @[handle] | Xk | X% | R$ X | Alto | 2 |

## Briefing Padrão

**Produto:** [descrição]
**Mensagem-chave:** [o que comunicar]
**Obrigatório:** [menção, link, hashtag, CTA]
**Proibido:** [o que não pode fazer/falar]
**Formato:** [tipo de conteúdo]
**Prazo:** [datas]
**Entregáveis:** [o que entregar para aprovação]

## Métricas

| KPI | Meta | Como Medir |
|-----|------|-----------|
| Alcance | [X] | Relatório do influencer |
| Impressões | [X] | Relatório do influencer |
| Cliques | [X] | UTM + analytics |
| Conversões | [X] | Cupom exclusivo ou UTM |
| CPE (Custo por Engajamento) | R$ [X] | Budget / engajamentos |
| ROI | [X]x | Receita / investimento |
```

## Regras
- Engagement rate > número de seguidores (micro influencer com 5% > macro com 1%)
- Sempre use UTM ou cupom exclusivo para rastrear resultados
- Briefing claro mas não engessado — deixe o creator ser autêntico
- Contrato por escrito SEMPRE (direitos de imagem, exclusividade, prazo)
- Peça acesso às métricas reais (prints de insights, não números "estimados")
- Para conversão: micro e nano influencers múltiplos > 1 macro
- Inclua cláusula de boost (direito de impulsionar o conteúdo do influencer como ad)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-persona` — use o output como input se já foi rodada
- `/marketing-campanha` — use o output como input se já foi rodada

### Passa o bastão para:
- **Conteúdo do influencer → boost como ad** → `/meta-copy-criativo`
- **Resultados → relatório** → `/meta-relatorio-performance`

### Contexto compartilhado
Influencer é um canal dentro da campanha. Métricas devem ser consolidadas com ads.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
