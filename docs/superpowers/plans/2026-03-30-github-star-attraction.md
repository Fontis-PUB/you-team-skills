# GitHub Star Attraction — Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Ship the visual and content upgrades to make `claude-code-skills` star-attractive on GitHub, then push to remote.

**Architecture:** All changes are in `claude-code-skills/` — a rewritten bilingual README, two SVG assets (banner + chains diagram), and a CONTRIBUTING.md. No build pipeline, no dependencies. Pure markdown + SVG.

**Tech Stack:** SVG, GitHub Markdown, shields.io badges, git

---

### Task 1: Verify SVGs render correctly

**Files:**
- Read: `claude-code-skills/assets/banner.svg`
- Read: `claude-code-skills/assets/chains-diagram.svg`

- [ ] **Step 1: Open banner in browser**

```bash
open /Users/brabus/Documents/GitHub/You-team-skills/you-team-skills/claude-code-skills/assets/banner.svg
```

Expected: Dark background (#0d0d1a), purple→cyan top bar, neon grid icon on the left, white monospace title "you-team-skills", purple subtitle, grey stats line, cyan bottom bar.

- [ ] **Step 2: Open chains diagram in browser**

```bash
open /Users/brabus/Documents/GitHub/You-team-skills/you-team-skills/claude-code-skills/assets/chains-diagram.svg
```

Expected: Dark background, 6 rows of pill-shaped nodes, each chain in a distinct neon color (orange/purple/cyan/green/yellow/pink), arrows between nodes, footer text.

- [ ] **Step 3: Verify README renders (preview locally)**

```bash
open /Users/brabus/Documents/GitHub/You-team-skills/you-team-skills/claude-code-skills/README.md
```

Or use VS Code Markdown Preview. Expected: banner image at top, 5 purple badges, bilingual HTML tables, collapsible `<details>` sections for each of the 8 areas.

---

### Task 2: Add CONTRIBUTING.md

**Files:**
- Create: `claude-code-skills/CONTRIBUTING.md`

- [ ] **Step 1: Create CONTRIBUTING.md**

Create the file at `claude-code-skills/CONTRIBUTING.md` with this exact content:

```markdown
# Contributing / Contribuindo

## Adding a new skill / Adicionando uma nova skill

1. Create a folder inside the appropriate area:

```bash
mkdir claude-code-skills/01-gestao-trafego/my-new-skill
touch claude-code-skills/01-gestao-trafego/my-new-skill/SKILL.md
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
```

- [ ] **Step 2: Verify the file was created**

```bash
cat /Users/brabus/Documents/GitHub/You-team-skills/you-team-skills/claude-code-skills/CONTRIBUTING.md | head -20
```

Expected: Shows the YAML frontmatter section at the top.

---

### Task 3: Commit all changes

**Files:**
- Stage: `claude-code-skills/README.md`
- Stage: `claude-code-skills/assets/banner.svg`
- Stage: `claude-code-skills/assets/chains-diagram.svg`
- Stage: `claude-code-skills/CONTRIBUTING.md`

- [ ] **Step 1: Check git status**

```bash
cd /Users/brabus/Documents/GitHub/You-team-skills/you-team-skills && git status
```

Expected: Shows modified `claude-code-skills/README.md` and untracked `claude-code-skills/assets/` and `claude-code-skills/CONTRIBUTING.md`.

- [ ] **Step 2: Stage the files**

```bash
cd /Users/brabus/Documents/GitHub/You-team-skills/you-team-skills && \
git add claude-code-skills/README.md \
        claude-code-skills/assets/banner.svg \
        claude-code-skills/assets/chains-diagram.svg \
        claude-code-skills/CONTRIBUTING.md
```

- [ ] **Step 3: Verify staged files**

```bash
cd /Users/brabus/Documents/GitHub/You-team-skills/you-team-skills && git diff --staged --stat
```

Expected: 4 files listed with insertions.

- [ ] **Step 4: Commit**

```bash
cd /Users/brabus/Documents/GitHub/You-team-skills/you-team-skills && git commit -m "$(cat <<'EOF'
feat: bilingual README, hero banner SVG, chains diagram, CONTRIBUTING

- Rewrite README to EN/PT-BR bilingual with HTML table layout
- Add assets/banner.svg: dark neon hero (1280x320, purple/cyan palette)
- Add assets/chains-diagram.svg: 6 handoff chains visualized (neon nodes)
- Add CONTRIBUTING.md with skill quality checklist
- Collapsible <details> sections for all 8 team areas

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>
EOF
)"
```

Expected: `[main <hash>] feat: bilingual README...` with 4 files changed.

---

### Task 4: Push to GitHub (manual approval required)

- [ ] **Step 1: Verify remote**

```bash
cd /Users/brabus/Documents/GitHub/You-team-skills/you-team-skills && git remote -v
```

Expected: Shows `origin` pointing to `github.com/fontiss/claude-code-skills` (or the actual remote URL).

- [ ] **Step 2: Push** ⚠️ Confirm with user before running

```bash
cd /Users/brabus/Documents/GitHub/You-team-skills/you-team-skills && git push origin main
```

Expected: `Branch 'main' set up to track remote branch 'main' from 'origin'.`

---

### Task 5: GitHub repo settings (manual — no CLI)

These must be done in the GitHub web UI at `github.com/<user>/claude-code-skills` → Settings.

- [ ] **Step 1: Set repository description**

Go to repo home page → click the ⚙️ gear icon next to "About".

Set description to:
```
56 Claude Code Skills — Your complete business team. Traffic, launches, social media, sales, marketing, strategy, design & ops. Bilingual EN/PT-BR.
```

- [ ] **Step 2: Set website**
Leave blank or set to your personal site / product page.

- [ ] **Step 3: Add topics**

In the same "About" panel, add these topics:
```
claude-code  ai-agents  llm  claude  skills  marketing  business  brazil  open-source  productivity
```

- [ ] **Step 4: Verify social preview**

Go to Settings → General → Social preview. The `assets/banner.svg` is NOT automatically used as social preview (GitHub requires a raster image for that). To use the banner:

Option A — Upload manually: Settings → General → Social preview → Upload image. Screenshot the banner.svg from a browser (1280×640 recommended) and upload.

Option B — Add Open Graph image to repo: Create a `assets/social-preview.png` by screenshotting the SVG in a browser, then upload via GitHub UI.

---

### Task 6: Verify everything on GitHub

- [ ] **Step 1: Check README renders**

Visit `github.com/<user>/claude-code-skills` and confirm:
- Banner SVG visible at top
- 5 purple badges visible
- Bilingual tables render correctly
- `<details>` sections are collapsible
- Chains diagram visible

- [ ] **Step 2: Check badge URLs resolve**

Click each badge. All shields.io badges should load (green/purple, not broken).

- [ ] **Step 3: Confirm repo has topics**

Topics should appear as grey pills below the description on the repo home page.

---

## Post-launch checklist / Checklist pós-lançamento

- [ ] Share on Twitter/X with the EN tagline + repo link
- [ ] Post in Brazilian Claude/AI communities (Telegram, Discord)
- [ ] Submit to `awesome-claude` or similar lists if they exist
- [ ] Monitor GitHub Traffic tab (Insights → Traffic) after 48h
