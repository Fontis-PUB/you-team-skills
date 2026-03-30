---
name: comercial-proposta
description: Cria propostas comerciais profissionais com escopo, investimento, diferenciais e termos. Use quando o usuário pedir proposta comercial, orçamento para cliente, documento de proposta, precificação de serviço, ou apresentação de oferta B2B/B2C.
---

# Proposta Comercial

Crie propostas profissionais que vendem valor antes de apresentar preço.

## Estrutura da Proposta

```markdown
# Proposta Comercial
**Para:** [Nome do Cliente / Empresa]
**De:** [Sua Empresa]
**Data:** [dd/mm/yyyy]
**Validade:** [X dias]

---

## 1. Contexto e Diagnóstico
[Demonstre que você entendeu o problema do cliente — 3-5 parágrafos]
- Situação atual
- Desafios identificados
- Impacto de não resolver (custo da inação)

## 2. Solução Proposta
[O que você vai entregar — claro e específico]

### Escopo de Trabalho

| # | Entrega | Descrição | Prazo |
|---|---------|-----------|-------|
| 1 | [entrega] | [detalhamento] | [X dias/semanas] |
| 2 | [entrega] | [detalhamento] | [X dias/semanas] |
| 3 | [entrega] | [detalhamento] | [X dias/semanas] |

### O que NÃO está incluído
- [item fora do escopo 1]
- [item fora do escopo 2]
(Evita scope creep e alinha expectativas)

## 3. Resultados Esperados
[Métricas ou outcomes tangíveis]
- [resultado 1 com número/prazo]
- [resultado 2 com número/prazo]

## 4. Diferenciais
[Por que escolher você — 3-4 pontos com evidência]
- [diferencial + prova]

## 5. Cases / Prova Social
[1-2 cases relevantes com resultado]
> "[Depoimento curto do cliente]" — Nome, Cargo, Empresa

## 6. Investimento

| Plano | Inclui | Investimento |
|-------|--------|-------------|
| [Essencial] | [escopo reduzido] | R$ X/mês ou R$ X total |
| [Profissional] | [escopo completo] | R$ X/mês ou R$ X total |
| [Premium] | [escopo + extras] | R$ X/mês ou R$ X total |

**Condições:** [parcelamento, desconto à vista, forma de pagamento]
**Início:** Após aprovação e pagamento da primeira parcela

## 7. Cronograma

| Semana | Atividade | Entrega |
|--------|-----------|---------|
| 1 | [fase] | [marco] |
| 2-3 | [fase] | [marco] |
| 4 | [fase] | [entrega final] |

## 8. Termos e Condições
- Validade da proposta: [X] dias
- Prazo de execução: [X] dias/semanas após aprovação
- Cancelamento: [condições]
- Propriedade intelectual: [quem fica com o quê]

## Próximos Passos
1. Aprovação desta proposta
2. Assinatura do contrato
3. Pagamento inicial
4. Kickoff em [data]

---
**[Nome] | [Cargo] | [Email] | [Telefone]**
```

## Regras
- Sempre apresente 2-3 opções de plano (ancoragem — o do meio costuma ser o escolhido)
- Diagnóstico vem ANTES do preço — venda o problema antes da solução
- Inclua "O que NÃO está incluído" para evitar scope creep
- Validade de 7-15 dias cria urgência sem pressão
- Para propostas acima de R$10K: inclua ROI estimado
- Proposta deve ser PDF ou DOCX profissional, nunca texto corrido no WhatsApp
- Linguagem: confiante mas não arrogante, específica mas não técnica demais

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/whatsapp-atendimento` — use o output como input se já foi rodada
- `/negocios-precificacao` — use o output como input se já foi rodada

### Passa o bastão para:
- **Proposta enviada → follow-up** → `/comercial-follow-up`
- **Proposta aceita → onboarding** → `/ops-cs`
- **Proposta recusada → registrar motivo** → `/comercial-crm`

### Contexto compartilhado
Precificação deve vir de `/negocios-precificacao`. Diagnóstico inicial deve refletir o que foi descoberto no atendimento.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
