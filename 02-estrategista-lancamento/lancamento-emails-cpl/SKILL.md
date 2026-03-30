---
name: lancamento-emails-cpl
description: Cria sequências completas de emails para fase de CPL (Conteúdo de Pré-Lançamento) — convites, lembretes, replays e aquecimento entre aulas. Use quando o usuário pedir emails de CPL, sequência de emails para aulas de lançamento, emails de lembrete de live, emails de replay, ou comunicações da fase de pré-lançamento.
---

# Emails de CPL (Pré-Lançamento)

Crie sequências de email para cada CPL do lançamento, maximizando presença e engajamento.

## Sequência Padrão por CPL

Para cada aula/conteúdo de pré-lançamento:

1. **Convite (D-2):** Apresenta o tema + promessa específica da aula + data/hora
2. **Lembrete D-1:** Reforça o benefício + cria antecipação com teaser
3. **Lembrete D0 (3h antes):** Urgência + link direto
4. **Lembrete D0 (15min):** "Estamos ao vivo" — link + 1 frase
5. **Replay (D+1):** Recap dos pontos principais + link do replay + prazo para assistir
6. **Replay urgência (D+2):** "Sai do ar amanhã" + gancho para próxima aula

## Estrutura de Cada Email

```
ASSUNTO: [máx 50 chars — curiosidade ou benefício específico]
PREVIEW TEXT: [máx 90 chars — complementa o assunto]

[Hook — 1-2 linhas que conectam com a dor/desejo]

[Corpo — 3-5 parágrafos curtos, máx 3 linhas cada]

[CTA claro — botão ou link com texto de ação]

[P.S. — gatilho extra: escassez, prova social, ou teaser]
```

## Regras de Assuntos

Fórmulas que funcionam para CPLs:
- Curiosidade: "O erro que custa R$X por mês (aula ao vivo)"
- Benefício direto: "Como [resultado] em [prazo] — aula gratuita"
- Número: "3 passos para [resultado] (aula 2 de 4)"
- Pessoal: "[Nome], reservei isso para você"
- Urgência: "Começa em 2 horas — sua vaga está garantida?"

## Gatilhos por Aula

- **CPL 1 (Oportunidade):** Curiosidade + novidade
- **CPL 2 (Transformação):** Prova social + história
- **CPL 3 (Método):** Autoridade + especificidade
- **CPL 4 (Oferta):** Antecipação + escassez

## Regras
- Emails curtos (150-250 palavras máx) — mobile first
- 1 CTA por email, repetido no máximo 2x (meio + final)
- Personalização com nome quando possível
- Replay deve incluir timestamp dos momentos-chave da aula
- Nunca envie mais de 2 emails por dia (exceto dia do evento)
- Tom conversacional — como se estivesse mandando para um amigo
- Inclua P.S. em todo email — é a segunda linha mais lida depois do assunto

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/lancamento-cronograma` — use o output como input se já foi rodada
- `/lancamento-copy` — use o output como input se já foi rodada

### Passa o bastão para:
- **CPLs finalizados → preparar carrinho** → `/lancamento-emails-carrinho`
- **Métricas de presença** → `/lancamento-metricas`

### Contexto compartilhado
Assuntos e hooks devem seguir a mesma narrativa dos copies de `/lancamento-copy`.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
