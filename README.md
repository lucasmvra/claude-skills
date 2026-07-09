# claude-skills

Central source of truth for Claude Code skills, shared across projects via git submodule.

Each top-level directory is a skill (contains a `SKILL.md`). Mount this repo into a
project at `.claude/skills/` and Claude Code will load every skill here.

## Use in a project

```bash
git submodule add https://github.com/lucasmvra/claude-skills .claude/skills
git submodule update --init --remote
```

A `SessionStart` hook in each project runs `git submodule update --init --remote`
so fresh sessions always have the latest skills.

## Add a new skill

Drop a `<skill-name>/SKILL.md` folder here, commit, push. Every project that uses
this submodule picks it up on its next session (or `git submodule update --remote`).

## Included skills

- **ui-ux-pro-max** — UI/UX design intelligence (styles, palettes, typography, charts, stacks)
- **ui-styling** — Tailwind / shadcn styling, theming, accessibility
- **design-system** — design tokens, component specs, slides
- **design** — logo, icon, CIP, social/slide design
- **brand** — brand voice, visual identity, messaging
- **slides** — HTML presentations
- **banner-design** — banners for social/ads/web/print

Sourced from https://github.com/nextlevelbuilder/ui-ux-pro-max-skill (MIT).
