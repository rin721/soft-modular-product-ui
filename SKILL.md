---
name: playful-video-platform-ui
description: Use to generate light, playful, pink-accented UI for video platforms, creator communities, product hubs, landing pages, mobile pages, dashboards, and component specs. Applies a distilled media-community visual language with slim navigation, soft cards, dense content grids, acrylic overlays, geometric decoration, responsive rules, interaction states, and validation checks. Do not use for cloning kirakira.moe or copying its brand assets, logo, imagery, text, or proprietary data.
---

# Playful Video Platform UI

Use this skill to generate a reusable UI system inspired by the observed visual language of `https://kirakira.moe`, not to copy that site. The output should feel light, playful, content-first, creator-community oriented, and technically implementable.

## Read Order

1. Read this file first.
2. Use `design-tokens.json` for implementation values.
3. Read `style-profile.md`, `layout-patterns.md`, and `component-recipes.md` when generating full pages.
4. Read `interaction-rules.md` and `responsive-rules.md` before coding states or breakpoints.
5. Read `adaptation-rules.md` when changing colors, fonts, density, or product tone.
6. Use `prompt-templates.md` and `examples/` for reusable generation prompts.
7. Run `validation-checklist.md` before final delivery.

## When To Use

- Generate UI for video platforms, creator communities, product hubs, media libraries, fan communities, app dashboards, and landing pages.
- Create component specs or frontend recipes with soft cards, small radii, pink accent, acrylic overlays, slim navigation, and dense media grids.
- Convert a rough product brief into a polished, playful, light-content UI.
- Adapt the design language to another brand while keeping its layout grammar and interaction rhythm.

## When Not To Use

- Do not use this skill to clone `kirakira.moe`, recreate its logo, copy its exact graphics, reuse its screenshots, reuse its icons, or copy its proprietary copy and data.
- Do not use it for heavy enterprise dashboards that require dense tables, neutral-only palettes, or formal institutional tone.
- Do not use it for brutalist, luxury editorial, dark cyberpunk, skeuomorphic, or ornate decorative styles without an adaptation pass.
- Do not use it when exact source-site pixel parity is requested.

## Trigger Phrases

- "Use playful-video-platform-ui"
- "Generate a light pink video platform UI"
- "Make a creator community homepage"
- "Build a soft anime-adjacent product page"
- "Create a content grid with playful navigation"
- "Design a mobile page in this distilled UI language"
- "Create component recipes for this pink creator platform style"

## Input Contract

Accept these inputs when provided. If missing, infer conservative defaults and list assumptions.

- `page_type`: homepage, landing page, product page, content grid, dashboard, mobile page, component spec.
- `audience`: creators, viewers, fans, enterprise buyers, community members, admins.
- `content_domain`: video, music, learning, design, gaming, SaaS, documentation, events.
- `primary_goal`: browse, search, upload, join, buy, learn, configure, contact.
- `required_sections`: list of sections or components that must appear.
- `brand_overrides`: accent color, typography, density, radius, tone, dark mode.
- `framework`: HTML/CSS, React, Vue, Tailwind, design spec, or markdown-only.
- `responsive_targets`: desktop, tablet, mobile, or exact viewport list.
- `accessibility_level`: baseline, WCAG AA, reduced motion, keyboard-first.
- `copy_tone`: playful, product-led, corporate, premium, minimal, technical.

## Output Contract

Every generated UI or spec must include:

- Page structure and section order.
- Token mapping from `design-tokens.json`.
- Component recipes used, including hover, active, focus, disabled, loading, and error where relevant.
- Responsive behavior for desktop, tablet, and mobile.
- Accessibility notes for color contrast, keyboard focus, semantic roles, touch target size, and reduced motion.
- Originality check confirming no copied source-site assets, logo, text, screenshots, icons, or data.
- Uncertainty labels for anything inferred rather than observed.

## Execution Steps

1. Classify the requested `page_type` and audience.
2. Select the closest layout grammar from `layout-patterns.md`.
3. Apply the aesthetic profile from `style-profile.md`.
4. Map colors, typography, spacing, radius, shadows, motion, breakpoints, and z-index from `design-tokens.json`.
5. Choose component recipes from `component-recipes.md`; do not invent incompatible variants until the base recipes are covered.
6. Add interaction states from `interaction-rules.md`.
7. Apply responsive rules from `responsive-rules.md`, with mobile overflow checks.
8. If brand changes are requested, apply `adaptation-rules.md` after preserving the app-shell, grid, card, and motion grammar.
9. Produce the UI, component spec, or prompt output requested by the user.
10. Validate with `validation-checklist.md`.

## Core Design Principles

- Keep the page light: white or near-white canvas, soft pink accent, gray text, and low-contrast surfaces.
- Use slim persistent navigation: left rail on desktop/tablet, top appbar plus bottom nav on mobile.
- Make content browseable: media cards, category rows, badges, tags, and metadata should be compact but readable.
- Favor soft acrylic and shadow over heavy borders.
- Keep radii small for cards and controls: mostly `4px` and `6px`, with pills only for tags and nav ripples.
- Add playful geometry sparingly: diagonal bars, dots, oversized pale icons, simple line shapes, and accent blocks.
- Use springy but short motion. Interactions should feel responsive, not theatrical.
- Treat functionality seriously: forms, upload zones, modals, and error states must be clear and accessible.

## Design Token Rules

- Use `color.accent.primary` as the default accent unless `brand_overrides.accent` is provided.
- Generate accent ramps with `color-mix(in oklab, accent, white/black ...)` or equivalent if the framework supports it.
- Use `typography.base.size` `14px` and line-height `1.4` for normal UI text.
- Use the display stack for headings and large numbers; use the body stack for all UI text.
- Use spacing in multiples of `4px`, with `8`, `16`, `24`, and `26px 5dvw` as common layout anchors.
- Use `radius.sm` `4px`, `radius.md` `6px`, `radius.pill`, and `radius.circle`.
- Use soft shadows only. Avoid heavy elevation.
- Use motion tokens exactly unless the user requests reduced motion.

## Component Generation Rules

- Use icon buttons for navigation and compact actions.
- Use primary buttons only for decisive actions; use secondary/tertiary buttons for navigation and supporting actions.
- Use cards for individual repeated items, not as wrappers around whole page sections.
- Use 16:9 media thumbnails with rounded `6px` corners.
- Use badges and tags for counts, categories, filters, and state.
- Use forms with inset backgrounds, bottom focus stripe, trailing icons, and clear error states.
- Use modals and flyouts with acrylic blur, `6px` radius, soft shadow, and responsive bottom-sheet behavior on mobile.

## Responsive Rules

- Desktop `>991px`: left rail `56px`, content padding `26px 5dvw`, dense auto-fill grids.
- Tablet `640-991px`: keep left rail `56px`, content padding `24px`, reduce grid columns.
- Mobile `<=639px`: use top appbar `56px` and bottom nav `56px`; content padding `16px`; default to one-column cards unless two columns are explicitly safe.
- Never allow horizontal overflow on mobile. The source observation showed a mobile overflow risk; generated UI must fix it.
- Minimum touch target is `44px`; navigation touch targets may be `48px`.

## Interaction Rules

- Hover: soft background overlay, accent title color, or lift cards by about `6px`.
- Active: reduce shadow and scale to about `.9722`; icon-only controls may scale icon to `.9`.
- Focus: visible `3px` focus ring using accent or neutral gray.
- Disabled: reduce opacity, remove shadow, and suppress pointer events.
- Loading: use progress bars or rings in accent color; provide reduced-motion fallback.
- Transitions: default `0.25s cubic-bezier(.19,1,.22,1)`; springy movement `0.5s`; drawer/modal `0.6s`.
- Reduced motion: remove loops and large transforms; keep instant state changes.

## Adaptation Rules

- Replace the accent color by generating the full accent ramp, focus color, hover overlay, ripple, and shadow mix.
- Replace fonts only by preserving the split between expressive display face and highly legible UI body face.
- Adjust radius within `2px` to `10px`; keep components consistent.
- For corporate tone, reduce decorative geometry and playful copy, but keep light canvas, slim nav, card grid, and focus states.
- For premium tone, lower saturation and increase whitespace without increasing border radius dramatically.
- For minimal tone, remove most decoration but keep accent linework and interaction rhythm.

## Prohibitions

- Do not copy the source site's logo, wordmark, mascot, icons, video thumbnails, banners, category names as a fixed dataset, user names, or proprietary copy.
- Do not embed source-site screenshots or remote asset URLs.
- Do not reproduce the exact page structure mechanically.
- Do not use large rounded cards, heavy dark gradients, purple-blue gradient blobs, ornate illustrations, or one-note pink surfaces.
- Do not omit mobile behavior, focus states, disabled states, loading states, or uncertainty labels.
- Do not present inferred rules as observed facts.

## Example Calls

```text
Use playful-video-platform-ui to create a mobile-first landing page for a creator analytics tool. Audience: independent video creators. Primary goal: start a free trial. Framework: React + CSS modules.
```

```text
Use playful-video-platform-ui to design a component spec for navigation, media cards, tags, forms, and modals. Include desktop, tablet, and mobile states.
```

```text
Use playful-video-platform-ui with brand_overrides.accent = #2f80ed and copy_tone = corporate to generate a product homepage for a B2B media workflow platform.
```

## Quality Checklist

- Confirm the design is a reusable style, not a source-site clone.
- Confirm all colors, spacing, radii, shadows, motion, and breakpoints map to tokens.
- Confirm each component has hover, active, focus, disabled, and loading/error states where relevant.
- Confirm desktop, tablet, and mobile layouts are specified.
- Confirm mobile has no horizontal overflow.
- Confirm decorative elements are generic and original.
- Confirm accessibility notes are present.
- Confirm observed, inferred, and unverified items are labeled.

