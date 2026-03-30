# Contributing / Contribuindo

## Adding a new skill / Adicionando uma nova skill

1. Create a folder inside the appropriate area:

```bash
mkdir 01-gestao-trafego/my-new-skill
touch 01-gestao-trafego/my-new-skill/SKILL.md
```

2. Every `SKILL.md` must start with YAML frontmatter:

```yaml
---
name: my-new-skill
description: Describe exactly when Claude Code should trigger this skill. Be specific — use keywords your users will say.
---
```

3. Structure your skill with:
   - **Workflow** — numbered steps the skill follows
   - **Output template** — exact markdown the skill should produce
   - **Team integration** — who passes context in, who receives the handoff

4. Open a PR. Title format: `feat: add [skill-name] to [area]`

## Improving an existing skill / Melhorando uma skill existente

- Open an issue describing the benchmark or framework you want to update
- PRs welcome — include a before/after example of the output difference

## Skill quality bar / Barra de qualidade

- [ ] Has YAML frontmatter with `name` and `description`
- [ ] `description` contains 3+ trigger phrases users would actually say
- [ ] Output uses traffic-light scoring (🟢🟡🔴) where applicable
- [ ] Ends with a `## 🔄 Próximo Passo do Time` handoff block
- [ ] Brazilian market benchmarks are sourced or noted as estimates

## License / Licença

By contributing, you agree your code is MIT licensed.
