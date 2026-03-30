---
name: design-apresentacao
description: Estrutura e cria apresentações visuais profissionais — slides, decks, keynotes com hierarquia visual e storytelling. Use quando o usuário pedir para criar apresentação, deck de slides, PowerPoint, keynote, ou estruturar conteúdo visual para apresentação.
---

# Design de Apresentação

Estruture apresentações com hierarquia visual, storytelling e impacto.

## Princípios

1. **1 ideia por slide** — se precisa ler, está errado
2. **Visual > texto** — use imagens, gráficos, ícones
3. **Hierarquia clara** — headline → suporte → detalhe
4. **Consistência** — mesma paleta, tipografia, layout em todo deck
5. **Storytelling** — início (problema) → meio (jornada) → fim (solução/CTA)

## Estrutura por Tipo

### Apresentação Institucional (10-15 slides)
1. Capa (marca + tagline)
2. Quem somos
3. Problema que resolvemos
4. Nossa solução
5. Como funciona
6. Diferenciais
7. Resultados/Cases (2-3 slides)
8. Clientes/Parceiros
9. Equipe
10. Contato/CTA

### Apresentação de Resultados (8-12 slides)
1. Capa
2. Contexto/Objetivo
3. Resumo executivo
4. Resultados principais (dados visuais)
5-8. Detalhamento por área
9. Aprendizados
10. Próximos passos

### Workshop/Treinamento (15-30 slides)
1. Capa + agenda
2. Contexto/por que importa
3-25. Conteúdo em blocos (conceito → exemplo → exercício)
26. Resumo
27. Q&A
28. Recursos adicionais

## Output

```markdown
# 🖥️ Estrutura de Apresentação — [Título]
**Formato:** [16:9 / 4:3]
**Slides:** [X]
**Duração:** [X minutos]
**Público:** [quem vai assistir]

## Direção Visual
- **Paleta:** [cores com HEX]
- **Fonte headline:** [nome]
- **Fonte corpo:** [nome]
- **Estilo:** [minimalista/corporativo/criativo/dark]
- **Elementos:** [fotos/ícones/ilustrações/gráficos]

## Slide a Slide

### Slide 1: Capa
**Layout:** [central / split / full-bleed image]
**Headline:** [título]
**Subtítulo:** [contexto]
**Visual:** [descrição da imagem/background]

### Slide 2: [Título]
**Layout:** [2 colunas / lista / gráfico / imagem + texto]
**Headline:** [texto — máx 8 palavras]
**Corpo:** [bullet points — máx 3, máx 10 palavras cada]
**Visual:** [ícone/gráfico/foto]
**Notas do apresentador:** [talking points]

[Repetir para cada slide]

## Notas de Design
- [Transições sugeridas]
- [Animações (se aplicável)]
- [Fonte de dados para gráficos]
```

## Regras
- Máximo 20 palavras por slide (exceção: slides de dados)
- Headlines: 6-8 palavras, impactantes
- Gráficos: 1 por slide, com legenda clara e insight no título
- Fotos: alta resolução, sem marcas d'água
- Fundos: consistentes (não alterne branco/escuro aleatoriamente)
- Para apresentar ao vivo: menos texto, mais visual (a fala complementa)
- Para enviar por email: mais texto (precisa funcionar sem apresentador)
- Slide de transição entre blocos ajuda a respirar e organizar

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-pitch` — use o output como input se já foi rodada
- `/design-brand` — use o output como input se já foi rodada

### Contexto compartilhado
Paleta, tipografia e estilo devem seguir brand guide.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
