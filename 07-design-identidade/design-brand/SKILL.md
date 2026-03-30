---
name: design-brand
description: Documenta e estrutura brand books, manuais de identidade visual e guidelines de marca. Use quando o usuário pedir brand book, manual de marca, identidade visual documentada, guidelines de design, padrões visuais, ou sistema de identidade de marca.
---

# Brand Book / Manual de Marca

Documente a identidade visual completa da marca com guidelines claros.

## Estrutura do Brand Book

```markdown
# 📖 Brand Book — [Marca]
**Versão:** [X.X]
**Data:** [mm/yyyy]

---

## 1. A Marca

### Propósito
[Por que a marca existe — 1-2 frases]

### Missão
[O que faz e para quem]

### Visão
[Onde quer chegar]

### Valores
1. [Valor 1] — [descrição curta]
2. [Valor 2] — [descrição curta]
3. [Valor 3] — [descrição curta]

### Personalidade da Marca
- **Arquétipos:** [primário + secundário]
- **Tom de voz:** [formal/casual/provocativo/empático]
- **Adjetivos:** [5 palavras que descrevem a marca]
- **Se a marca fosse uma pessoa:** [descrição]

---

## 2. Logo

### Versão Principal
[Descrição + uso correto]

### Variações
- Horizontal / Vertical / Ícone
- Positiva (fundo claro) / Negativa (fundo escuro)
- Monocromática

### Área de Proteção
[Espaço mínimo ao redor do logo — definir em unidade X]

### Tamanho Mínimo
- Digital: [Xpx de largura]
- Impresso: [Xmm de largura]

### Uso Incorreto (DON'Ts)
- Não distorcer
- Não alterar cores
- Não adicionar efeitos (sombra, brilho)
- Não usar sobre fundos que comprometam legibilidade
- Não rotacionar

---

## 3. Cores

### Paleta Principal
| Nome | HEX | RGB | CMYK | Pantone | Uso |
|------|-----|-----|------|---------|-----|
| [Primary] | #XXXXX | X,X,X | X,X,X,X | XXXX C | Elementos principais |
| [Secondary] | #XXXXX | X,X,X | X,X,X,X | XXXX C | Acentos |
| [Dark] | #XXXXX | X,X,X | X,X,X,X | — | Textos |
| [Light] | #XXXXX | X,X,X | X,X,X,X | — | Fundos |

### Paleta de Apoio
[Cores complementares para gráficos, ilustrações, etc]

### Proporção de Uso
- Primary: 60%
- Secondary: 30%
- Accent: 10%

---

## 4. Tipografia

### Fonte Principal (headlines)
- **Família:** [nome]
- **Pesos:** [Regular, Bold, etc]
- **Uso:** Títulos, destaques, CTAs
- **Fallback:** [fonte alternativa]

### Fonte Secundária (corpo)
- **Família:** [nome]
- **Pesos:** [Regular, Medium, etc]
- **Uso:** Textos corridos, UI, documentos
- **Fallback:** [fonte alternativa]

### Hierarquia Tipográfica
| Nível | Fonte | Peso | Tamanho | Line-height |
|-------|-------|------|---------|-------------|
| H1 | [X] | Bold | [X]px | [X] |
| H2 | [X] | Bold | [X]px | [X] |
| H3 | [X] | Medium | [X]px | [X] |
| Body | [X] | Regular | [X]px | [X] |
| Caption | [X] | Regular | [X]px | [X] |

---

## 5. Elementos Visuais

### Iconografia
- Estilo: [outline / filled / duotone]
- Espessura de traço: [Xpx]
- Fonte: [biblioteca ou custom]

### Fotografia
- Estilo: [natural / editorial / lifestyle / product]
- Tratamento: [filtro, cor, contraste]
- Temas: [o que mostrar / o que evitar]

### Ilustrações (se aplicável)
- Estilo: [flat / 3D / hand-drawn / geometric]
- Paleta: [seguir paleta principal / paleta específica]

### Patterns e Texturas
[Descrição e uso]

---

## 6. Aplicações

### Digital
- Social media: templates e grid
- Website: screenshots e guidelines
- Email: header e assinatura

### Impresso
- Cartão de visita
- Papelaria
- Embalagem

### Assinatura de Email
```
[Nome Completo]
[Cargo] | [Empresa]
[email] | [telefone]
[site]
```
```

## Regras
- Brand book é documento vivo — versione e atualize
- Inclua exemplos de uso CORRETO e INCORRETO para cada elemento
- Forneça arquivos em todos os formatos necessários (SVG, PNG, AI, PDF)
- Para startups: um brand book simples (logo + cores + tipografia + tom) é melhor que nenhum
- Tipografia: máximo 2 famílias (1 display + 1 corpo)
- Cores: máximo 5 na paleta principal (menos = mais consistente)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-persona` — use o output como input se já foi rodada
- `/design-naming` — use o output como input se já foi rodada

### Passa o bastão para:
- **Brand definida → briefings futuros** → `/design-briefing`
- **Brand → todos os copies** → `/instagram-copy`

### Contexto compartilhado
O tom de voz definido aqui deve ser seguido por TODAS as skills de comunicação.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
