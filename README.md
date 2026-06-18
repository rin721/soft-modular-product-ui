# Playful Video Platform UI Skill

This repository contains a universal UI Design Skill distilled from observations of `https://kirakira.moe`. It is not a copy of that site. It packages a reusable visual language for agents that need to generate light, playful, media-community interfaces with slim navigation, soft cards, pink accent, dense content grids, acrylic overlays, and responsive interaction states.

The skill is designed for Codex, Claude Code, OpenClaw, Hermes, and other agents that can read Markdown and JSON. It does not require a private plugin protocol.

## What This Is

- A reusable design system and generation guide.
- A documentation-only skill package with structured tokens and modular recipes.
- A way to create new homepages, landing pages, product sections, mobile screens, and component specs inspired by the source site's visual grammar.

## What This Is Not

- Not a clone generator for the source site.
- Not a bundle of source images, logos, icons, screenshots, videos, or proprietary copy.
- Not a static analysis report. The files are written as instructions an AI agent can execute.

## Evidence Source

Observed pages:

- `https://kirakira.moe/`
- `https://kirakira.moe/category`
- `https://kirakira.moe/search`
- `https://kirakira.moe/upload`
- `https://kirakira.moe/video/kv1`

Observed implementation signals:

- Nuxt-rendered HTML and CSS assets.
- Desktop, tablet, and mobile screenshots.
- CSS variables, breakpoints, component state rules, shadows, typography, radii, and motion timings.

External skill-structure references:

- OpenAI Codex Skills documentation.
- Claude Agent Skills documentation.
- Agent Skills specification.
- Claude slash command documentation.

## File Structure

```text
/
├── SKILL.md
├── README.md
├── design-tokens.json
├── style-profile.md
├── layout-patterns.md
├── component-recipes.md
├── interaction-rules.md
├── responsive-rules.md
├── adaptation-rules.md
├── prompt-templates.md
├── validation-checklist.md
└── examples/
    ├── landing-page.md
    ├── corporate-homepage.md
    ├── product-section.md
    └── mobile-page.md
```

## How Agents Should Use It

1. Load `SKILL.md` as the entrypoint.
2. Use `design-tokens.json` as the source of implementation values.
3. Read the rule file that matches the task: style, layout, components, interaction, responsive, adaptation, prompts, or validation.
4. Generate an original UI for the user's product, audience, and content.
5. Run the validation checklist before final delivery.

## Maintenance

- Update `design-tokens.json` when new measured values are discovered.
- Update `component-recipes.md` when new component behavior is observed or intentionally added.
- Keep `SKILL.md` concise and link to sibling files for detail.
- Keep all values labeled with `source` and `confidence`.
- Preserve the anti-copying boundary whenever extending examples.

## Uncertainty Policy

Observed facts come from screenshots, SSR HTML, and CSS. Inferred rules are marked where the original behavior was not directly verified. Unverified areas include authenticated states, exact runtime behavior for some menus, full dark-mode rendering, and some expanded form/modal states.

