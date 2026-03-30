---
name: design-briefing
description: Cria briefings completos para projetos de design — logos, identidade visual, materiais gráficos, embalagens e campanhas visuais. Use quando o usuário pedir briefing de design, brief criativo, documento para designer, especificação visual, ou quando precisar comunicar direções visuais para um designer ou equipe criativa.
---

# Design Briefing

Crie briefings estruturados que eliminam retrabalho e alinham expectativas.

## Estrutura do Briefing

```markdown
# 📐 Briefing de Design — [Projeto]
**Solicitante:** [nome]
**Data:** [dd/mm/yyyy]
**Prazo:** [data de entrega]
**Prioridade:** [alta/média/baixa]

## 1. Contexto do Projeto
- **Marca/Empresa:** [nome]
- **Segmento:** [nicho]
- **Público-alvo:** [quem vai ver/usar o material]
- **Objetivo:** [o que o design precisa FAZER — informar, converter, impressionar]

## 2. Escopo da Entrega
- **Peça(s):** [logo / post Instagram / apresentação / embalagem / etc]
- **Formatos:** [dimensões, orientação, digital/impresso]
- **Variações:** [light/dark, horizontal/vertical, com/sem tagline]
- **Arquivos finais:** [AI, PSD, PNG, SVG, PDF — especificar]

## 3. Direção Visual

### Referências (moodboard)
- [Link/descrição de referência 1 — o que gosta nela]
- [Link/descrição de referência 2 — o que gosta nela]
- [Link/descrição de referência 3 — o que gosta nela]

### Estilo Desejado
- **Mood:** [minimalista / luxuoso / vibrante / corporativo / orgânico / tech]
- **Cores:** [paleta existente ou direção: "tons escuros", "cores quentes"]
- **Tipografia:** [serif/sans-serif, peso, estilo — ou "a definir"]
- **Elementos:** [fotos, ilustrações, ícones, patterns, texturas]

### O que NÃO Queremos
- [estilo/elemento/cor a evitar]
- [referência negativa — "nada parecido com X"]

## 4. Conteúdo
- **Textos:** [copy exato que vai na peça, incluindo headline, corpo, CTA]
- **Imagens:** [fotos fornecidas, banco de imagens, IA, ilustração]
- **Logo:** [arquivo anexo ou link]
- **Brand guide:** [link ou "não existe ainda"]

## 5. Restrições Técnicas
- [Resolução mínima para impressão: 300dpi]
- [Cores CMYK para impressão / RGB para digital]
- [Tamanho máximo de arquivo]
- [Plataforma: Instagram, LinkedIn, site, outdoor — cada um tem specs]

## 6. Processo de Aprovação
- **Rodada 1:** [data] — conceitos iniciais (2-3 opções)
- **Rodada 2:** [data] — refinamento da opção escolhida
- **Final:** [data] — ajustes finais e entrega de arquivos
- **Aprovador:** [quem decide]

## 7. Checklist de Entrega
- [ ] Peça principal em todos os formatos solicitados
- [ ] Variações (se aplicável)
- [ ] Arquivos editáveis (fonte/layers)
- [ ] Versões para diferentes tamanhos/plataformas
- [ ] Mockups de aplicação
```

## Regras
- Briefing vago = resultado aleatório. Seja específico em tudo
- SEMPRE inclua referências visuais (links, screenshots, moodboard)
- Inclua o que NÃO quer (evita direção errada)
- Textos devem estar APROVADOS antes de ir para design
- Para projetos de identidade visual: inclua valores da marca, personalidade, arquétipos
- Cada peça = 1 briefing (não misture logo + site + embalagem no mesmo brief)
- Defina número de rodadas de revisão no briefing (evita escopo infinito)

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-persona` — use o output como input se já foi rodada
- `/design-brand` — use o output como input se já foi rodada

### Passa o bastão para:
- **Briefing pronto → execução** → `/design-ui-ux`

### Contexto compartilhado
Se brand guide existe, referencie. Se persona existe, inclua no público do briefing.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
