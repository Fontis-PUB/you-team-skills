---
name: lancamento-oferta
description: Estrutura ofertas irresistíveis para lançamentos — stack de valor, bônus, garantia, ancoragem de preço e condições. Use quando o usuário pedir para montar uma oferta, criar stack de valor, definir preço de lançamento, estruturar bônus, ou criar a composição de oferta para venda.
---

# Estruturação de Oferta

Monte ofertas com stack de valor claro, ancoragem de preço e estrutura que maximiza conversão.

## Componentes da Oferta

1. **Produto Core** — o que o cliente compra
2. **Bônus** — aceleradores de resultado (3-5 ideais)
3. **Garantia** — redutor de risco (7, 15, 30 dias)
4. **Ancoragem** — valor percebido vs. preço real
5. **Condições** — parcelamento, desconto à vista, early bird
6. **Escassez real** — vagas, prazo, bônus limitado

## Output

```markdown
# 💰 Estrutura de Oferta — [Produto]

## Produto Principal
**Nome:** [nome comercial]
**Promessa central:** [transformação em 1 frase]
**Formato:** [curso/mentoria/serviço/SaaS]
**Valor percebido:** R$ [X]

## Stack de Valor

| # | Item | Formato | Valor Percebido |
|---|------|---------|-----------------|
| 1 | [Produto core] | [X módulos/Y horas] | R$ X |
| 2 | Bônus: [nome] | [formato] | R$ X |
| 3 | Bônus: [nome] | [formato] | R$ X |
| 4 | Bônus: [nome] | [formato] | R$ X |
| 5 | Bônus: [nome] | [formato] | R$ X |
| — | **Valor Total** | — | **R$ X** |

## Preço e Condições
- **Preço de lançamento:** R$ X (desconto de Y% vs. valor total)
- **À vista (PIX):** R$ X (desconto extra de Z%)
- **Parcelado:** até 12x de R$ X no cartão
- **Early Bird (primeiras Xh):** bônus extra [nome]

## Garantia
- **Tipo:** [Incondicional / Condicional]
- **Prazo:** [7/15/30 dias]
- **Mecanismo:** [devolução integral / crédito]
- **Copy:** "[frase da garantia]"

## Ancoragem na Página de Vendas
"Separadamente, tudo isso custaria R$ [valor total].
Mas hoje, neste lançamento, seu investimento é de apenas R$ [preço]."
```

## Regras
- Valor percebido do stack deve ser 5-10x o preço real
- Bônus devem acelerar o resultado do produto core (não ser coisas aleatórias)
- Pelo menos 1 bônus deve ter escassez real (prazo ou vagas)
- Garantia incondicional para ticket < R$500, condicional para > R$500
- Nunca sugira preços inflados artificialmente para "ancoragem" — o valor percebido deve ser justificável
- Inclua sempre opção PIX com desconto (reduz inadimplência e taxas de gateway)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-persona` — use o output como input se já foi rodada
- `/negocios-precificacao` — use o output como input se já foi rodada
- `/marketing-concorrentes` — use o output como input se já foi rodada

### Passa o bastão para:
- **Oferta definida → escrever página** → `/lancamento-pagina`
- **Oferta definida → escrever emails** → `/lancamento-emails-carrinho`
- **Precificação precisa de análise** → `/negocios-precificacao`

### Contexto compartilhado
Use a persona para definir o que valoriza. Use a análise de concorrentes para diferenciar.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
