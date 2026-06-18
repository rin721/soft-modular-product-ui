# Style Profile

## Aesthetic Profile

Keywords: soft, playful, creator-community, light, pink-accented, content-first, low-radius, airy-but-dense, anime-adjacent, video-platform adjacent, app-like.

The visual language balances a mostly white workspace with a vivid warm pink accent. It uses small-radius surfaces, compact metadata, slim navigation, and playful geometric decoration to keep the interface friendly without turning it into a toy-like landing page.

## Observed Evidence

- The homepage uses a white canvas with warm pink brand-scale decoration, a fixed slim left rail, a horizontal category nav, an announcement card, and a dense media-card grid.
- Tablet keeps the left rail and reduces grid density.
- Mobile uses a top appbar and bottom navigation. A 390px capture showed horizontal overflow risk in a two-column media grid.
- Search uses a centered stage with large brand-style title, segmented control, and an inset search box.
- Category uses two-column list cards with icon, label, and small pink count badge.
- Upload uses a warning info bar, dashed dropzone, and compact stat cards.
- Video detail uses a large media/player area with pale pink geometric decoration and compact action metadata.

## Brand Mood

- Friendly and community-led.
- Technically competent but not corporate-heavy.
- Playful through motion, geometry, and accent color rather than through cartoon illustration.
- Optimistic and lightweight.

## Visual Density

Use medium density. Navigation and metadata can be compact, but primary content should breathe. Dense media grids are acceptable because each card has a fixed thumbnail ratio, short title, metadata, and clear hover response.

## Space And Composition

- Large canvas areas are allowed, especially for search, upload, player, or hero modes.
- Content pages prefer left alignment after the app shell.
- Search and empty states may be centered.
- Decorative geometry lives at edges or behind primary content and must not reduce readability.

## Color Tendencies

- Main canvas: white or near-white.
- Accent: warm pink `#f06e8e`.
- Text: near-black gray, not pure black unless needed.
- Metadata/icons: muted neutral-gray mixed with accent.
- Functional states may use orange, green, red, blue, cyan, and purple, but these should not dominate the theme.

## Typography

- Use an expressive geometric display face for headings, stats, and logo-like text.
- Use a highly legible multilingual sans stack for body and UI.
- Use compact text sizes: base `14px`, metadata `12px`, subheaders `16px`, display titles around `40px`.
- English display headings may use italic or high weight. CJK headings may use skew or small-caps-like emphasis only when legible.

## Image And Icon Style

- Media thumbnails should be real content previews or neutral placeholders, always 16:9 and clipped to `6px`.
- Icons should be solid, simple, and familiar.
- Decorative icons can be oversized, pale, and partially off-canvas.
- Do not use the source site's actual icons, logo, screenshots, or thumbnails.

## Suitable Use Cases

- Creator community homepage.
- Media browsing interface.
- Product hub for creator tools.
- Youthful SaaS landing page.
- Mobile app shell for content discovery.
- Component system for content cards, tags, search, upload, and modals.

## Unsuitable Use Cases

- Formal finance, legal, or medical interfaces.
- Dense admin data tables where emotion should disappear.
- Luxury editorial pages with oversized photography and serif typography.
- Dark-only cyberpunk products.
- Exact brand replication or source-site cloning.

## Transferable Principles

- Use one warm accent to organize active state and visual rhythm.
- Keep card radius small and shadows soft.
- Preserve content-first hierarchy: thumbnails, title, metadata, then actions.
- Use playful decoration as background signal, not as content.
- Make every interaction feel soft and springy but quick.
- Fix mobile overflow and accessibility issues rather than reproducing them.

