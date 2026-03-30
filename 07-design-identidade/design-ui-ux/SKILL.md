---
name: design-ui-ux
description: Especifica interfaces e experiências de usuário — wireframes textuais, user flows, componentes, design system e heurísticas. Use quando o usuário pedir wireframe, especificação de interface, user flow, design de tela, UX review, design system, ou documentação de UI/UX.
---

# Design UI/UX

Especifique interfaces e experiências de usuário com clareza para desenvolvedores e designers.

## Entregáveis

### 1. User Flow
Mapeamento da jornada do usuário passo a passo.

```markdown
## User Flow — [Funcionalidade]

[Trigger] → Tela 1: [nome]
    → Ação A → Tela 2: [nome]
        → Sucesso → Tela 3: [confirmação]
        → Erro → Modal: [mensagem de erro]
    → Ação B → Tela 4: [nome]
```

### 2. Wireframe Textual
Especificação detalhada de cada tela sem precisar de ferramenta visual.

```markdown
## Tela: [Nome]
**URL:** /[path]
**Objetivo:** [o que o usuário faz aqui]

### Header
- Logo (esquerda)
- Menu: [Home] [Produtos] [Contato] [Login]
- CTA: [Botão primário]

### Hero Section
- Headline: [H1 — placeholder]
- Subheadline: [texto]
- CTA Button: [texto do botão] → [destino]
- Imagem: [descrição]

### Seção 2: [Nome]
- [Layout: 3 colunas]
- Card 1: [ícone] + [título] + [descrição]
- Card 2: [ícone] + [título] + [descrição]
- Card 3: [ícone] + [título] + [descrição]

### Footer
- [Colunas: links, social, newsletter, legal]

### Comportamento
- **Mobile:** [como adapta — stack vertical, menu hamburger, etc]
- **Hover:** [estados de hover em botões, cards]
- **Loading:** [skeleton/spinner/progressbar]
- **Empty state:** [o que mostra quando não há dados]
- **Error state:** [como exibe erros]
```

### 3. Design System (Componentes)

```markdown
## Design System — [Projeto]

### Tokens
- **Cores:** [primary, secondary, neutral, success, warning, error]
- **Tipografia:** [font-family, sizes, weights]
- **Spacing:** [4px grid: 4, 8, 12, 16, 24, 32, 48, 64]
- **Border-radius:** [4px, 8px, 12px, full]
- **Shadows:** [sm, md, lg]

### Componentes

#### Button
| Variante | Background | Text | Border | Uso |
|----------|-----------|------|--------|-----|
| Primary | [cor] | white | none | CTAs principais |
| Secondary | transparent | [cor] | [cor] | CTAs secundários |
| Ghost | transparent | [cor] | none | Ações terciárias |
| Destructive | red | white | none | Ações destrutivas |

**Estados:** default, hover, active, disabled, loading
**Tamanhos:** sm (32px), md (40px), lg (48px)

#### Input
[mesma estrutura]

#### Card
[mesma estrutura]

#### Modal
[mesma estrutura]
```

### 4. UX Review (Avaliação Heurística)

```markdown
## UX Review — [Produto/Tela]

| # | Heurística | Status | Issue | Recomendação |
|---|-----------|--------|-------|-------------|
| 1 | Visibilidade do status | 🟢🟡🔴 | [issue] | [fix] |
| 2 | Compatibilidade sistema-mundo | 🟢🟡🔴 | [issue] | [fix] |
| 3 | Controle e liberdade | 🟢🟡🔴 | [issue] | [fix] |
| 4 | Consistência e padrões | 🟢🟡🔴 | [issue] | [fix] |
| 5 | Prevenção de erros | 🟢🟡🔴 | [issue] | [fix] |
| 6 | Reconhecimento > memorização | 🟢🟡🔴 | [issue] | [fix] |
| 7 | Flexibilidade e eficiência | 🟢🟡🔴 | [issue] | [fix] |
| 8 | Design minimalista | 🟢🟡🔴 | [issue] | [fix] |
| 9 | Recuperação de erros | 🟢🟡🔴 | [issue] | [fix] |
| 10 | Ajuda e documentação | 🟢🟡🔴 | [issue] | [fix] |
```

## Regras
- Wireframe textual deve ser claro o suficiente para um dev implementar sem dúvidas
- Sempre especifique estados: default, hover, active, disabled, loading, empty, error
- Mobile first — especifique comportamento responsivo
- Acessibilidade: contraste mínimo 4.5:1, labels em inputs, keyboard navigation
- Componentes reutilizáveis > design custom por tela
- Para UX Review: baseie nas 10 heurísticas de Nielsen

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/design-briefing` — use o output como input se já foi rodada
- `/ops-produto` — use o output como input se já foi rodada

### Passa o bastão para:
- **Specs prontas → desenvolvimento** → `/ops-produto`

### Contexto compartilhado
PRD vem de `/ops-produto`. Design system deve seguir o brand guide.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
