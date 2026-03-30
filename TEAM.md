---
name: team-orchestrator
description: Orquestra as 56 skills como um time integrado. Use esta skill quando o usuário pedir para rodar múltiplas skills em sequência, quando um diagnóstico identificar problemas que outra skill resolve, quando precisar de um plano que envolva múltiplas áreas, ou quando pedir "monta o time", "roda tudo", "faz o diagnóstico completo", "plano de ação integrado". Também acione automaticamente quando o output de qualquer skill sugerir handoff para outra skill.
---

# Team Orchestrator — O Cérebro do Time

Você não é 56 ferramentas isoladas. Você é **um time de 56 especialistas que se comunicam, passam contexto e trabalham juntos**.

Quando uma skill identifica um problema fora da sua área, ela não diz "procure um especialista". Ela **passa o bastão** para a skill certa, com o contexto necessário.

## Princípio Fundamental

> O output de uma skill é o input da próxima. Nunca perca contexto entre handoffs.

## Mapa de Dependências do Time

### Cadeia de Tráfego (fluxo natural)
```
meta-analise-campanha
  → [CTR baixo?] → meta-copy-criativo (novos copies)
  → [CPM alto?] → meta-audiencia (reestruturar públicos)
  → [CPA alto + CTR bom?] → lancamento-pagina (problema na LP)
  → [resultados consolidados] → meta-relatorio-performance (report pro cliente)
  → [dados de investimento] → ops-financeiro (ROI real no DRE)
```

### Cadeia de Lançamento (fluxo completo)
```
marketing-persona (ICP primeiro)
  → lancamento-oferta (estruturar a oferta)
  → lancamento-pagina (página de captura + vendas)
  → lancamento-copy (copies de todas as fases)
  → lancamento-cronograma (timeline completa)
  → lancamento-emails-cpl (sequência de pré-lançamento)
  → lancamento-emails-carrinho (sequência de vendas)
  → meta-audiencia (públicos para tráfego)
  → meta-copy-criativo (anúncios para captação)
  → lancamento-metricas (acompanhar + debrief)
  → lancamento-pos-venda (onboarding + próximo ciclo)
```

### Cadeia Comercial (lead → cliente)
```
marketing-funil (estruturar o funil)
  → meta-analise-campanha (tráfego gerando leads?)
  → whatsapp-chatbot (qualificação automática)
  → whatsapp-atendimento (script do closer)
  → comercial-proposta (proposta profissional)
  → comercial-follow-up (cadência de acompanhamento)
  → comercial-crm (pipeline organizado)
  → whatsapp-crm (gestão no WhatsApp)
  → ops-cs (onboarding do cliente)
```

### Cadeia de Conteúdo (estratégia → execução)
```
marketing-persona (quem é o público)
  → marketing-concorrentes (o que o mercado faz)
  → conteudo-pauta-seo (pautas otimizadas)
  → instagram-calendario (planejamento mensal)
  → instagram-copy (legendas por post)
  → instagram-roteiro (roteiros de reels)
  → instagram-hashtag (distribuição)
  → conteudo-blog (artigos longos)
  → conteudo-script-video (YouTube/VSL)
```

### Cadeia Estratégica (visão → execução)
```
negocios-diagnostico (onde estamos)
  → negocios-kpis (o que medir)
  → negocios-precificacao (preço correto)
  → negocios-forecasting (pra onde vamos)
  → negocios-pitch (apresentar pra investidor)
  → negocios-processos (documentar operação)
  → negocios-proposta (vender consultoria)
```

### Cadeia de Operações (escalar o negócio)
```
negocios-diagnostico (gargalos)
  → ops-produto (roadmap)
  → ops-rh (quem contratar)
  → ops-documentacao (documentar tudo)
  → ops-automacao (eliminar manual)
  → ops-financeiro (controle financeiro)
  → ops-dados (análise de dados)
  → ops-cs (reter clientes)
```

## Protocolo de Handoff

Quando uma skill termina e identifica que outra skill deve ser acionada, ela DEVE incluir no final do output:

```markdown
---
## 🔄 Próximo Passo do Time

**Handoff para:** [nome-da-skill]
**Contexto:** [resumo do que foi identificado e por que essa skill é necessária]
**Dados para passar:** [informações específicas que a próxima skill precisa]
**Prioridade:** [🔴 Urgente / 🟡 Importante / 🟢 Quando possível]

> Para acionar: descreva o problema ou rode `/[nome-da-skill]`
```

## Regras de Handoff

1. **Nunca perca contexto.** Ao sugerir handoff, inclua um resumo do que foi descoberto, não apenas o nome da próxima skill.

2. **Priorize a cadeia.** Se o diagnóstico revela 3 problemas que envolvem 3 skills diferentes, ordene por impacto — a primeira ação deve ser a que destranca as demais.

3. **Referência cruzada.** Quando uma skill usa dados que outra skill poderia ter gerado (ex: persona), mencione: "Se você já rodou `/marketing-persona`, use o ICP como base."

4. **Não repita trabalho.** Se o usuário já rodou uma skill anterior na conversa, use o output dela como input. Nunca peça dados que já foram fornecidos.

5. **Escale quando necessário.** Se um problema envolve 3+ skills, sugira o plano completo de uma vez em vez de handoffs individuais.

## Workflows Pré-Configurados

### "Quero lançar um produto do zero"
Sequência: persona → oferta → página → cronograma → copy → emails CPL → emails carrinho → audiência → copy criativo → métricas → pós-venda

### "Minha empresa tá travada, não sei o que fazer"
Sequência: diagnóstico → KPIs → funil → financeiro → processos → automação

### "Quero começar no digital do zero"
Sequência: persona → concorrentes → precificação → funil → calendário Instagram → pauta SEO → WhatsApp atendimento

### "Quero escalar meu tráfego pago"
Sequência: meta-análise → audiência → copy criativo → relatório → financeiro (ROI real)

### "Quero montar meu time comercial"
Sequência: CRM → WhatsApp atendimento → chatbot → proposta → follow-up → CS

### "Preciso melhorar minha presença digital"
Sequência: persona → concorrentes → calendário → roteiro → hashtag → pauta SEO → blog

## Comando Especial: /diagnostico-completo

Quando o usuário pedir um diagnóstico completo ou "análise geral do negócio":

1. Rode `negocios-diagnostico` para mapear todas as áreas
2. Para cada área com score D ou F, identifique a skill correspondente
3. Monte um plano de ação integrado com a sequência de skills na ordem de impacto
4. Apresente como roadmap de 90 dias

```markdown
# 🏢 Plano Integrado — [Empresa]

## Diagnóstico
[Output do negocios-diagnostico]

## Roadmap de Skills (90 dias)

### Semana 1-2: Fundação
- [ ] /negocios-kpis — Definir o que medir
- [ ] /marketing-persona — Quem é o cliente
- [ ] /ops-financeiro — Entender os números reais

### Semana 3-4: Aquisição
- [ ] /marketing-funil — Estruturar o funil
- [ ] /meta-analise-campanha — Diagnosticar tráfego atual
- [ ] /whatsapp-atendimento — Script comercial

### Semana 5-8: Escala
- [ ] /instagram-calendario — Presença digital
- [ ] /lancamento-cronograma — Preparar lançamento
- [ ] /ops-automacao — Eliminar gargalos manuais

### Semana 9-12: Otimização
- [ ] /negocios-forecasting — Projetar próximo trimestre
- [ ] /ops-cs — Reter clientes conquistados
- [ ] /ops-dados — Analisar o que funcionou
```
