---
name: GitHub Star Attraction — you-team-skills
description: Design spec for making the you-team-skills repo visually compelling and star-attractive on GitHub
type: project
---

# GitHub Star Attraction Design

**Date:** 2026-03-30
**Project:** you-team-skills / claude-code-skills
**Goal:** Maximize GitHub stars — 60% Brazilian audience, 40% global

## Target Audience
- Primary (60%): Brazilian digital marketers, infoproductors, agency owners, traffic managers
- Secondary (40%): Global Claude Code users, AI power-users, indie hackers

## Visual Identity
- Style: Energetic/digital — purple/neon (like modern AI products: Vercel, Linear, Replicate)
- Primary colors: `#7c3aed` (violet), `#a855f7` (purple), `#06b6d4` (cyan)
- Background: `#0d0d1a` (very dark navy)
- Font: system-ui / sans-serif (no external dependencies)

## Language Strategy
- Bilingual side-by-side: EN (left) / PT-BR (right) using HTML tables
- Section headers: `## English / Português`
- Code blocks: unified (bash is the same in both languages)

## Deliverables

### 1. `claude-code-skills/assets/banner.svg`
- 1280×320px
- Dark background with purple→cyan gradient accent lines
- 3×3 grid icon (neon, left side)
- Title: "you-team-skills" (large, white, with glow)
- Subtitle: bilingual EN/PT-BR
- Stats: "56 specialists · 8 areas · 6 handoff chains"

### 2. `claude-code-skills/assets/chains-diagram.svg`
- Shows all 6 handoff chains as horizontal pipelines
- Each chain: distinct neon color
- Pill-shaped nodes → arrows → next node
- Dark background

### 3. `claude-code-skills/README.md` (rewrite)
Structure:
1. Centered banner image
2. Centered shields.io badges (for-the-badge style, purple palette)
3. Bilingual tagline (HTML table)
4. Install in 30s (unified code)
5. The Team / O Organograma (8 area tables)
6. How the team works together (chains-diagram.svg + handoff example)
7. Workflows table
8. FAQ (bilingual)
9. License

## Success Criteria
- First 5 seconds: visitor sees banner + badges + bilingual tagline = instant "I want this"
- Scroll depth 1: install command visible without scrolling on desktop
- Scroll depth 2: chains diagram shows the "system" concept visually
- Star rate: target 10+ stars per week organically from GitHub Explore
