---
name: Guide Skill Design
description: Design spec for GUIDE.md — interactive onboarding skill for the 56-skill business team
type: project
---

# GUIDE.md Design Spec

**Date:** 2026-03-30
**File to create:** `GUIDE.md` at repo root
**Language:** PT-BR only
**Compatibility:** Claude Code (skill via /guide) + Claude chat (paste file content)

## Purpose
Single interactive skill that onboards any user into the 56-skill team. Starts with 3 triage questions, delivers a personalized action plan, and provides a full skill catalog with example prompts.

## Structure

### Part 1 — YAML Frontmatter
- `name: guide`
- `description:` contains all trigger phrases (começar, qual skill, plano, /guide, /guia, etc.)

### Part 2 — Triage (3 questions, one at a time, multiple choice)
1. Tipo de negócio (A-E)
2. Maior dor/objetivo (A-F)
3. Urgência (A-C)

### Part 3 — Personalized Plan Output
- 3-5 recommended skills in order
- Exact prompt pre-filled with user's context for each skill
- Ask which to start with → trigger that skill immediately

### Part 4 — Full Catalog (56 skills × 8 areas)
Each skill entry:
- `name` in backticks
- **Quando usar:** 1-2 sentences
- **Prompt pra usar:** realistic example with BR context
- **O que entrega:** 1 sentence
- **Claude Code:** `/command`
- **No chat:** which file to paste

### Part 5 — How to Use Without Claude Code
Step-by-step for claude.ai / Cowork / any chat interface

## Success Criteria
- User goes from zero to first skill output in < 2 minutes
- Works identically in Claude Code and raw chat
- Every skill has a copy-paste-ready prompt with realistic BR context
