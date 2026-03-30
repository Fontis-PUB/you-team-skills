---
name: design-naming
description: Cria nomes para marcas, produtos, serviços e campanhas com análise de disponibilidade e justificativa estratégica. Use quando o usuário pedir nome para marca, naming, nome de produto, nome de empresa, brainstorming de nomes, ou nomenclatura de qualquer projeto/negócio.
---

# Naming

Crie nomes memoráveis com justificativa estratégica e verificação de viabilidade.

## Processo

### 1. Briefing de Naming
- O que é? (produto, marca, serviço, campanha)
- Público-alvo
- Posicionamento (premium, popular, tech, humano)
- Personalidade da marca (arquétipos, adjetivos)
- Território semântico (palavras relacionadas ao universo)
- Idioma (PT-BR, EN, híbrido, inventado)
- Restrições (palavras/sons a evitar)

### 2. Técnicas de Criação

| Técnica | Descrição | Exemplo |
|---------|-----------|---------|
| Descritivo | Diz o que faz | PayPal, YouTube |
| Neologismo | Palavra inventada | Google, Spotify |
| Acrônimo | Iniciais | IBM, NASA |
| Metáfora | Associação simbólica | Amazon, Apple |
| Fusão | Combina palavras | Instagram, Pinterest |
| Toponímia | Referência a lugar | Patagonia, Adobe |
| Personificação | Nome de pessoa | Mercedes, Tesla |
| Onomatopeia | Som | Zoom, Ping |
| Latim/Grego | Raízes clássicas | Volvo, Audi |

### 3. Critérios de Avaliação

| Critério | Peso | Avaliação |
|----------|------|-----------|
| Memorabilidade | ⭐⭐⭐ | Fácil de lembrar? |
| Pronunciabilidade | ⭐⭐⭐ | Fala fácil em PT-BR? |
| Disponibilidade (.com/.com.br) | ⭐⭐⭐ | Domínio livre? |
| Disponibilidade INPI | ⭐⭐ | Marca registrável? |
| Disponibilidade social (@) | ⭐⭐ | Handle livre? |
| Significado negativo | ⭐⭐⭐ | Nenhum em PT/EN/ES? |
| Escalabilidade | ⭐⭐ | Funciona se expandir? |
| Diferenciação | ⭐⭐ | Único no mercado? |

## Output

```markdown
# ✨ Naming — [Projeto]

## Briefing
[Resumo do posicionamento e personalidade]

## Território Semântico
[Mapa de palavras relacionadas ao universo da marca]

## Propostas

### Opção 1: [Nome]
- **Técnica:** [descritivo/neologismo/fusão/etc]
- **Significado:** [de onde vem e o que evoca]
- **Pronúncia:** [como se fala]
- **Domínio .com:** [disponível/indisponível]
- **Domínio .com.br:** [disponível/indisponível]
- **Instagram @:** [disponível/indisponível]
- **INPI:** [verificar em busca.inpi.gov.br]
- **Score:** [X/10]

### Opção 2: [Nome]
[mesma estrutura]

### Opção 3: [Nome]
[mesma estrutura]

### Opção 4: [Nome]
[mesma estrutura]

### Opção 5: [Nome]
[mesma estrutura]

## Ranking Final

| # | Nome | Memorável | Pronúncia | Domínio | Diferenciação | Score |
|---|------|-----------|-----------|---------|--------------|-------|
| 1 | [X] | ⭐⭐⭐ | ⭐⭐⭐ | ✅ | ⭐⭐⭐ | X/10 |
| 2 | [X] | ⭐⭐ | ⭐⭐⭐ | ✅ | ⭐⭐ | X/10 |

## Recomendação
[Qual escolher e por quê]
```

## Regras
- Mínimo 5 opções com técnicas variadas
- Sempre verifique domínio (.com e .com.br) e @ de Instagram
- Teste a pronúncia em português brasileiro (não pode soar estranho)
- Verifique significado negativo em outros idiomas (PT, EN, ES no mínimo)
- Nomes curtos (2-3 sílabas) são mais memoráveis
- Evite nomes que limitem o negócio a um produto/nicho específico
- Para tech/SaaS: preferência por .com ou .io
- Nomes inventados são mais fáceis de registrar mas mais difíceis de lembrar

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/marketing-persona` — use o output como input se já foi rodada
- `/marketing-concorrentes` — use o output como input se já foi rodada

### Passa o bastão para:
- **Nome definido → brand book** → `/design-brand`

### Contexto compartilhado
O nome deve ressoar com a persona e se diferenciar dos concorrentes.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
