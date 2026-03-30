---
name: negocios-processos
description: Documenta e otimiza processos de negócio — fluxos, SOPs, automações e melhoria contínua. Use quando o usuário pedir para documentar processo, criar SOP, mapear fluxo de trabalho, otimizar operação, ou padronizar procedimentos.
---

# Processos de Negócio

Documente, otimize e automatize processos operacionais.

## Tipos de Documento

### SOP (Standard Operating Procedure)
Passo a passo detalhado para executar uma tarefa específica.

### Fluxo de Processo
Mapeamento visual de um processo com etapas, decisões e responsáveis.

### Playbook
Guia completo de uma área/função com múltiplos SOPs e contexto.

## Output — SOP

```markdown
# 📋 SOP — [Nome do Processo]
**Área:** [X]
**Responsável:** [cargo]
**Frequência:** [diário/semanal/por demanda]
**Última atualização:** [data]
**Versão:** [X.X]

## Objetivo
[O que este processo faz e por que existe — 2-3 linhas]

## Pré-requisitos
- [Acesso/ferramenta necessária]
- [Informação prévia necessária]

## Passo a Passo

### Etapa 1: [Nome]
**Responsável:** [cargo]
**Tempo:** ~X minutos
1. [Ação específica]
2. [Ação específica]
3. [Ação específica]
**Resultado esperado:** [o que deve acontecer ao concluir]

### Etapa 2: [Nome]
[mesma estrutura]

### Etapa 3: [Nome]
[mesma estrutura]

## Checklist Resumido
- [ ] [Etapa 1]
- [ ] [Etapa 2]
- [ ] [Etapa 3]

## Exceções e Troubleshooting
| Situação | Ação |
|----------|------|
| [problema comum] | [solução] |
| [erro frequente] | [como resolver] |

## Métricas do Processo
- Tempo total esperado: X minutos
- Taxa de erro aceitável: <X%
- Responsável por revisão: [cargo]
- Frequência de revisão: [trimestral]
```

## Regras
- Escreva para alguém que nunca fez a tarefa — clareza > brevidade
- Cada etapa = 1 ação (não agrupe múltiplas ações)
- Inclua screenshots/exemplos quando possível
- Exceções e troubleshooting são essenciais — processos falham
- Defina responsável para CADA etapa (não "a equipe")
- Versione e date — processos desatualizados são piores que nenhum
- Automatize o que puder — se é repetitivo e previsível, não deveria ser manual

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/negocios-diagnostico` — use o output como input se já foi rodada

### Passa o bastão para:
- **Processos repetitivos → automatizar** → `/ops-automacao`
- **Processos documentados → wiki** → `/ops-documentacao`

### Contexto compartilhado
Processos manuais identificados no diagnóstico são candidatos a automação.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
