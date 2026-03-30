---
name: ops-documentacao
description: Cria documentação operacional — wikis, bases de conhecimento, SOPs, playbooks e README. Use quando o usuário pedir para documentar processos, criar wiki, base de conhecimento, knowledge base, documentação interna, playbook operacional, ou organizar informações da empresa.
---

# Documentação Operacional

Crie documentação clara, organizada e mantível.

## Tipos de Documento

| Tipo | Objetivo | Formato | Público |
|------|----------|---------|---------|
| SOP | Passo a passo de tarefa | Checklist | Executor |
| Playbook | Guia completo de área | Manual | Equipe/área |
| Wiki | Base de conhecimento | Artigos interligados | Toda empresa |
| README | Introdução a projeto/sistema | Markdown | Devs/novos membros |
| Runbook | Resposta a incidentes | Procedimento | Ops/suporte |
| Decision Log | Registro de decisões | Tabela cronológica | Liderança |

## Estrutura de Wiki/Knowledge Base

```markdown
# 📚 Knowledge Base — [Empresa]

## Estrutura de Navegação

### 🏢 Geral
- Sobre a empresa (missão, valores, cultura)
- Organograma
- Políticas (férias, home office, benefícios)
- Ferramentas e acessos

### 💼 Áreas
- Comercial / [playbook + SOPs]
- Marketing / [playbook + SOPs]
- Produto / [playbook + SOPs]
- Operações / [playbook + SOPs]
- Financeiro / [playbook + SOPs]

### 🔧 Técnico
- Stack e arquitetura
- Ambiente de desenvolvimento
- Deploy e CI/CD
- Troubleshooting

### 📖 Onboarding
- Guia do primeiro dia
- Quem é quem
- Ferramentas essenciais
- Primeiras tarefas por cargo
```

## Template de Documento

```markdown
# [Título do Documento]
**Área:** [X]
**Autor:** [nome]
**Última atualização:** [data]
**Versão:** [X.X]
**Status:** [rascunho/revisão/publicado/arquivado]

## TL;DR
[Resumo em 2-3 frases — o que este documento cobre]

## Contexto
[Por que este documento existe e quando consultar]

## Conteúdo
[O conteúdo principal, organizado com H2/H3]

## FAQ
[Perguntas comuns sobre o tema]

## Links Relacionados
- [documento relacionado 1]
- [documento relacionado 2]

## Changelog
| Data | Autor | Mudança |
|------|-------|---------|
| [data] | [nome] | [o que mudou] |
```

## Regras
- Todo documento precisa de: autor, data, versão e TL;DR
- Escreva para alguém que está vendo pela primeira vez
- Documentação desatualizada é pior que nenhuma — defina owner e frequência de revisão
- Use templates padronizados (consistência > criatividade em docs)
- Links entre documentos relacionados (não crie silos)
- Busca é essencial — use títulos claros e tags/categorias
- Prefira listas e tabelas a parágrafos longos
- Screenshots e exemplos visuais valem mais que descrições

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-processos` — use o output como input se já foi rodada

### Contexto compartilhado
Documente o que foi padronizado em `/negocios-processos`.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
