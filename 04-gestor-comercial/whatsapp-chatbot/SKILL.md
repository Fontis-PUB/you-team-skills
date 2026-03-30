---
name: whatsapp-chatbot
description: Projeta fluxos de chatbot para WhatsApp com árvores de decisão, qualificação automática e encaminhamento para humano. Use quando o usuário pedir fluxo de chatbot, automação de WhatsApp, bot de atendimento, árvore de decisão, ou estrutura de automação para WhatsApp Business.
---

# WhatsApp Chatbot

Projete fluxos de chatbot inteligentes que qualificam, atendem e convertem.

## Componentes do Fluxo

1. **Mensagem de boas-vindas** — apresentação + menu de opções
2. **Qualificação** — perguntas de filtro (2-3 máx)
3. **Roteamento** — direcionar para o caminho correto
4. **Entrega de valor** — resposta, conteúdo ou ação
5. **Handoff** — transferência para humano quando necessário

## Output

```markdown
# 🤖 Fluxo Chatbot WhatsApp — [Negócio]

## Trigger: [primeiro contato / keyword / horário]

## Fluxo Principal

### Nó 1: Boas-vindas
**Mensagem:**
"Olá! 👋 Bem-vindo à [Empresa].
Como posso te ajudar?

1️⃣ Quero conhecer os produtos
2️⃣ Já sou cliente e preciso de suporte
3️⃣ Quero falar com um consultor"

**Ação:** Aguardar resposta (1, 2 ou 3)

---

### Caminho 1: Produtos
**Nó 1.1:**
"Ótimo! Qual área te interessa?
A) [Produto/Categoria A]
B) [Produto/Categoria B]
C) [Produto/Categoria C]"

**Nó 1.2:** [baseado na resposta, enviar info + CTA]

**Nó 1.3:** Qualificação
"Para te indicar a melhor opção:
Qual seu orçamento estimado?
A) Até R$X
B) R$X a R$Y
C) Acima de R$Y"

**Nó 1.4:** [Lead qualificado → handoff para humano com contexto]

---

### Caminho 2: Suporte
[fluxo de suporte]

### Caminho 3: Consultor
[captura de dados → encaminha para humano]

---

## Fallback (resposta não reconhecida)
"Desculpe, não entendi. Pode escolher uma das opções acima?
Ou digite HUMANO para falar com um atendente."

## Fora de Horário
"Nosso horário de atendimento é de Seg-Sex, 8h às 18h.
Deixe seu nome e telefone que retornamos amanhã!"

## Diagrama de Fluxo
[Descrever fluxo em formato visual ou mermaid]
```

## Regras
- Máximo 3 níveis de profundidade antes de handoff humano
- Sempre ofereça opção de falar com humano em qualquer ponto
- Respostas rápidas (botões/números) > texto livre
- Timeout: se não responder em 24h, enviar lembrete suave
- Fallback amigável para respostas não reconhecidas
- Dados coletados pelo bot devem ir para CRM antes do handoff
- Bot não deve tentar fechar vendas complexas — qualificar e passar

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-funil` — use o output como input se já foi rodada
- `/marketing-persona` — use o output como input se já foi rodada

### Passa o bastão para:
- **Lead qualificado → atendimento humano** → `/whatsapp-atendimento`
- **Dados coletados → CRM** → `/whatsapp-crm`

### Contexto compartilhado
O chatbot é o primeiro filtro. Dados de qualificação devem ir pro CRM antes do handoff humano.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
