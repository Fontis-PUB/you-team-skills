---
name: design-prompts-ia
description: Cria prompts otimizados para geração de imagens com IA (Midjourney, DALL-E, Stable Diffusion, Leonardo, Ideogram). Use quando o usuário pedir prompts para IA de imagem, gerar arte com IA, criar imagens com Midjourney/DALL-E, ou precisar de prompts visuais para qualquer ferramenta de geração de imagens por IA.
---

# Prompts para IA de Imagem

Crie prompts estruturados que geram resultados profissionais em ferramentas de IA.

## Anatomia de um Prompt Eficaz

```
[Assunto principal] + [Descrição detalhada] + [Estilo artístico] + [Iluminação] + [Composição] + [Qualidade/Técnica] + [Parâmetros da ferramenta]
```

## Categorias de Prompt

### Fotografia Realista
```
[subject], [action/pose], [setting/background], [lighting: golden hour/studio/dramatic/soft], [camera: Canon EOS R5, 85mm lens, f/1.4], [shot type: close-up/full body/aerial], 8K, ultra-detailed, photorealistic
```

### Ilustração/Arte Digital
```
[subject], [art style: flat illustration/watercolor/vector/oil painting/anime], [color palette], [mood], by [artist reference], trending on artstation, detailed, vibrant
```

### Design/Branding
```
[type: logo/icon/pattern/mockup], [style: minimal/geometric/organic/vintage], [colors], [background], professional design, clean lines, vector quality
```

### Produto/E-commerce
```
[product] on [surface], [background: white/gradient/lifestyle], professional product photography, studio lighting, commercial quality, 8K
```

### Social Media
```
[scene/concept], [mood/aesthetic], Instagram-worthy, vibrant colors, [aspect ratio], modern design, trending
```

## Output

```markdown
# 🎨 Pack de Prompts — [Objetivo]

## Contexto
- **Ferramenta:** [Midjourney/DALL-E/Stable Diffusion/Leonardo]
- **Objetivo:** [o que precisa criar]
- **Estilo:** [referência visual]
- **Uso:** [social media/site/apresentação/impressão]

---

## Prompt 1 — [Descrição]

### Para Midjourney:
```
[prompt completo] --ar 16:9 --v 6.1 --s 750
```

### Para DALL-E:
```
[prompt adaptado — mais descritivo, sem parâmetros técnicos]
```

### Para Stable Diffusion:
```
Positive: [prompt]
Negative: [o que evitar: blurry, deformed, low quality, text, watermark]
Steps: 30 | CFG: 7 | Sampler: DPM++ 2M Karras
```

## Prompt 2 — [Descrição]
[mesma estrutura]

## Prompt 3 — [Descrição]
[mesma estrutura]

---

## Dicas de Iteração
- Se muito genérico: adicione [detalhes específicos]
- Se estilo errado: especifique [estilo + artista referência]
- Se cores erradas: defina [paleta explícita]
- Se composição errada: especifique [camera angle + framing]
```

## Cheat Sheet de Parâmetros Midjourney

| Parâmetro | Uso | Valores |
|-----------|-----|---------|
| --ar | Aspect ratio | 1:1, 16:9, 9:16, 4:3 |
| --v | Versão | 6.1 (mais recente) |
| --s | Stylize | 0-1000 (750 = padrão) |
| --c | Chaos | 0-100 (variação) |
| --q | Quality | 0.25, 0.5, 1 |
| --no | Negative | --no text, watermark |
| --style | Sub-estilo | raw (menos estilizado) |

## Regras
- Seja específico: "mulher sorrindo" < "Brazilian woman in her 30s, warm smile, wearing white linen"
- Ordem importa: elementos no início do prompt têm mais peso
- Referências de artista/estilo são poderosas (adapte por ferramenta)
- Negative prompts são essenciais no Stable Diffusion (evitam defeitos)
- Para consistência de marca: inclua cores HEX e estilo específico em todo prompt
- Sempre entregue 3+ variações de prompt para o mesmo conceito
- DALL-E prefere linguagem natural; Midjourney prefere keywords separadas por vírgula

## 🔗 Integração com o Time

> Esta skill faz parte de um time de 56 especialistas que se comunicam. Consulte `TEAM.md` para o mapa completo de dependências.

### Recebe contexto de:
- `/design-briefing` — use o output como input se já foi rodada
- `/design-brand` — use o output como input se já foi rodada

### Contexto compartilhado
Cores e estilo devem seguir o brand guide.

### Protocolo de Handoff
Ao finalizar, se identificou um problema que outra skill resolve, inclua:
```
## 🔄 Próximo Passo do Time
**Handoff para:** /[skill]
**Contexto:** [o que foi descoberto]
**Dados para passar:** [informações relevantes]
**Prioridade:** 🔴/🟡/🟢
```
