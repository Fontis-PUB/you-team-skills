---
name: marketing-persona
description: Cria personas e ICPs (Ideal Customer Profile) detalhados com dados demográficos, psicográficos, dores, desejos e comportamento de compra. Use quando o usuário pedir para criar persona, ICP, perfil de cliente ideal, avatar de cliente, público-alvo detalhado, ou mapeamento de cliente.
---

# Persona e ICP

Crie perfis detalhados de cliente ideal que guiem toda a comunicação e estratégia.

## Diferença: Persona vs ICP

- **ICP (B2B):** Perfil da empresa ideal (tamanho, setor, faturamento, stack, dores organizacionais)
- **Persona (B2C/B2B):** Perfil da pessoa que toma ou influencia a decisão de compra

## Coleta
- Produto/serviço oferecido
- Clientes atuais (quem são os melhores?)
- Dados disponíveis (analytics, CRM, pesquisas)
- Nicho/mercado
- Ticket médio

## Output — Persona

```markdown
# 👤 Persona — [Nome fictício]

## Dados Demográficos
- **Nome:** [nome representativo]
- **Idade:** [faixa]
- **Gênero:** [X]
- **Localização:** [cidade/região]
- **Renda:** [faixa]
- **Escolaridade:** [nível]
- **Estado civil:** [X]
- **Profissão/cargo:** [X]

## Perfil Psicográfico
- **Valores:** [o que é importante na vida]
- **Estilo de vida:** [como vive o dia a dia]
- **Personalidade:** [introvertido/extrovertido, planejador/espontâneo, etc]
- **Aspirações:** [onde quer chegar em 1-3 anos]
- **Medos:** [o que teme]
- **Influências:** [quem segue, consome, admira]

## Relação com o Produto
- **Dor principal:** [problema #1 que o produto resolve]
- **Dores secundárias:** [2-3 outras dores]
- **Desejo principal:** [resultado #1 que busca]
- **Objeções:** [3-5 motivos para NÃO comprar]
- **Gatilhos de compra:** [o que faz decidir AGORA]
- **Jornada de compra:** [como pesquisa, compara, decide]

## Comportamento Digital
- **Redes sociais:** [quais usa, quanto tempo, como]
- **Conteúdo que consome:** [formatos, temas, criadores]
- **Horários online:** [quando está mais ativo]
- **Dispositivo principal:** [mobile/desktop]
- **Onde busca informação:** [Google, YouTube, Instagram, indicação]

## Frases que essa Pessoa Diz
- "[frase real que expressa a dor]"
- "[frase real que expressa o desejo]"
- "[frase real que expressa a objeção]"

## Mensagem-Chave (O que convence essa pessoa)
"[1 frase que conecta a dor com a solução de forma irresistível]"
```

## Output — ICP (B2B)

```markdown
# 🏢 ICP — Perfil de Cliente Ideal

## Empresa
- **Setor:** [X]
- **Tamanho:** [funcionários]
- **Faturamento:** [faixa]
- **Localização:** [região]
- **Maturidade digital:** [baixa/média/alta]
- **Stack atual:** [ferramentas que usa]

## Decisor
- **Cargo:** [X]
- **Dor:** [problema que sente]
- **Métrica que precisa melhorar:** [X]
- **Orçamento disponível:** [faixa]
- **Ciclo de decisão:** [X semanas/meses]

## Sinais de Compra
- [sinal 1 — ex: contratou gestor de tráfego recentemente]
- [sinal 2 — ex: está escalando vendas online]
- [sinal 3 — ex: postou sobre o problema no LinkedIn]

## Critérios de Qualificação

| Critério | Ideal | Aceitável | Desqualifica |
|----------|-------|-----------|-------------|
| Faturamento | >R$XM | R$X-XM | <R$X |
| Equipe | >X pessoas | X-X | <X |
| [critério] | [ideal] | [ok] | [não] |
```

## Regras
- Baseie em dados reais (clientes existentes) sempre que possível
- Frases do cliente devem soar naturais — como se você tivesse ouvido em uma pesquisa
- Persona com mais de 1 produto = 1 persona por produto/segmento
- ICP deve ter critérios de qualificação E desqualificação (economia de tempo do time comercial)
- Revise a cada 6 meses — personas mudam com o mercado
- Nunca crie persona genérica ("mulher, 25-45, classe B") — especificidade é o que gera valor

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-diagnostico` — use o output como input se já foi rodada

### Passa o bastão para:
- **Persona definida → TODAS as skills de comunicação** → `/instagram-copy`
- **ICP definido → qualificação comercial** → `/whatsapp-atendimento`
- **Persona → definir oferta** → `/lancamento-oferta`

### Contexto compartilhado
A persona é o fundamento. Praticamente todas as outras skills usam o output desta como base. Rode esta primeiro.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
