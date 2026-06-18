# Component Recipes

Each recipe includes usage, visual structure, token dependencies, state rules, responsive rules, forbidden deviations, and a generation example.

## Button

Usage: primary actions, secondary actions, icon actions, links that behave like buttons.

Visual structure:

- Primary: accent background, white text, `4px` radius, min-height `36px`, padding `8px 16px`.
- Secondary: transparent background, accent text, hover overlay.
- Tertiary/icon: transparent, muted icon color, circular touch/ripple area.

Token dependencies: `accent-primary`, `accent-hover`, `accent-focus`, `accent-pressed`, `accent-soft`, `radius-sm`, `shadow-hover`, `transition-default`, `transition-spring`.

State rules:

- Hover: accent-hover background and stronger soft shadow.
- Active: remove shadow and apply `scale(.9722)`.
- Focus: add `3px` accent focus ring.
- Disabled: use accent-disabled or gray, remove shadow, suppress pointer events.
- Loading: place a 2-4px progress bar at bottom or use an inline spinner.

Responsive rules:

- Desktop min-height `36px`.
- Mobile touch target at least `44px`; icon buttons can use `48px`.

Forbidden:

- Do not use heavy gradients or large pill buttons as the default.
- Do not hide focus rings.

Example:

```html
<button class="pv-button pv-button-primary">
  <span class="icon" aria-hidden="true"></span>
  <span>Start watching</span>
</button>
```

## Navigation

Usage: app shell, section navigation, bottom tabs, compact product navigation.

Visual structure:

- Desktop/tablet left rail: fixed `56px`, vertical icons, soft rail shadow.
- Mobile top appbar plus bottom nav: both `56px`.
- Active nav: accent icon, pale accent background, and an indicator.

Token dependencies: `accent-primary`, `accent-soft`, `icon-muted`, `shadow-rail`, `radius-circle`, `navigation` z-index.

State rules:

- Hover: soft overlay.
- Active: icon color accent and shortened indicator.
- Focus: visible ring around icon target.
- Disabled: muted gray and no pointer interaction.

Responsive rules:

- Switch from side rail to appbar/bottom nav at `<=639px`.
- Keep nav labels short on mobile.

Forbidden:

- Do not place a full desktop sidebar on mobile.
- Do not rely on color alone for active state.

Example:

```text
Desktop: rail(home, search, history, collections, upload, settings)
Mobile: appbar(menu, brand, profile) + bottom(home, categories, following)
```

## Hero

Usage: homepage banner, product landing intro, search stage, upload/player title region.

Visual structure:

- Use large display type with accent color.
- Add pale geometric decoration: diagonal bars, dots, simple line shapes, oversized icon silhouettes.
- Keep text readable and never inside a heavy card.

Token dependencies: `display` font, `page-title`, `accent-primary`, `accent-soft`, `desktop-container`, `transition-default`.

State rules:

- Decorative elements may fade or slide in once.
- Do not animate continuously unless reduced-motion fallback exists.

Responsive rules:

- Hide or simplify decorative banner on mobile when it steals space.
- Keep first actionable content visible.

Forbidden:

- Do not copy the source logo or star mark.
- Do not use stock-like dark hero photography for this style.

Example:

```text
Hero: product name, one-sentence value prop, primary CTA, secondary community link, pale diagonal accent block at top-right.
```

## Section

Usage: group content, feature list, grid, filters, announcements.

Visual structure:

- Section heading: icon + `16px` bold title + optional badge.
- Keep the section unframed; cards inside may be framed.
- Use `24px-48px` vertical gaps.

Token dependencies: `section-title`, `space-4`, `space-6`, `accent-primary`.

State rules:

- Section controls use button/tag rules.
- Empty/loading state uses ContentUnavailable or progress rules.

Responsive rules:

- Reduce vertical spacing on mobile.
- Keep headings on one row when possible, wrap gracefully.

Forbidden:

- Do not put a full page section inside a decorative card.

Example:

```text
Section header: icon, "Latest", count badge.
Body: responsive media grid.
```

## Card

Usage: media thumbnails, category rows, stat cards, feature cards.

Visual structure:

- Radius `6px`.
- Soft shadow only on elevated list/stat cards or hover.
- Media card: 16:9 cover, title, metadata lines.
- Category card: icon left, label, badge right.
- Stat card: icon/title top, large accent number bottom.

Token dependencies: `radius-md`, `shadow-card`, `surface-soft`, `caption`, `stat-number`, `card-hover-lift`.

State rules:

- Hover media card: lift `-6px`, add acrylic/soft shadow, title turns accent.
- Active: scale `.9722`, remove shadow.
- Focus: outer focus ring.
- Loading: use blurred placeholder or skeleton blocks, not copied thumbnails.

Responsive rules:

- Desktop grid uses minmax `226px`.
- Tablet about 3 columns.
- Mobile one column by default; two columns only if no overflow and text remains readable.

Forbidden:

- Do not use copied video thumbnails or names.
- Do not use oversized rounded cards.

Example:

```text
Card: 16:9 original placeholder or product image, 2-line title, muted metadata, compact icon row.
```

## Feature List

Usage: product features, benefits, categories, capabilities.

Visual structure:

- Use two-column or three-column card/grid on desktop.
- Each item has simple icon, short heading, one compact description.
- Use tags for feature status or category.

Token dependencies: `space-4`, `radius-md`, `icon-muted`, `accent-primary`, `shadow-card`.

State rules:

- Hover: icon or heading turns accent, card gets soft shadow.
- Focus: ring around item if clickable.

Responsive rules:

- Collapse to one column on mobile.

Forbidden:

- Do not write long marketing paragraphs inside feature cards.

Example:

```text
Feature item: icon, "Frame-accurate review", one sentence, "Beta" badge.
```

## Tag / Badge

Usage: categories, filters, counts, status, chips.

Visual structure:

- Badge: accent background, white text, `4px` radius, `0 8px` padding.
- Tag: pill background from neutral surface, `6px 12px`, optional checked icon.
- Checked tag: accent background, white text.

Token dependencies: `accent-primary`, `accented-selection`, `radius-sm`, `radius-pill`, `shadow-focus`.

State rules:

- Hover: soft shadow.
- Focus: neutral or accent focus ring.
- Checked: animated icon/spacing optional.
- Disabled: gray and no pointer interaction.

Responsive rules:

- Allow horizontal chip scrolling only when intentional and accessible.
- Wrap tags when they are filter content.

Forbidden:

- Do not overuse badges as decoration.

Example:

```text
Tags: "Tutorial", "Music", "Creator tools", checked "Latest".
```

## Form

Usage: search, login, settings, upload metadata, filters.

Visual structure:

- Text box: inset background, `6px` radius, `36px` normal height, `44px` large height.
- Focus stripe: 2px accent bottom stripe.
- Leading/trailing icons are muted until focus.
- Floating label only for large inputs.

Token dependencies: `inset-bg`, `radius-md`, `accent-primary`, `danger`, `focus-ring`, `space-3`.

State rules:

- Focus: accent stripe and leading icon.
- Invalid: red stripe and red label/icon.
- Disabled: reduced opacity, disabled cursor.
- Loading: trailing spinner or progress.

Responsive rules:

- Use large `44px` controls on mobile or touch-heavy screens.

Forbidden:

- Do not rely on placeholder-only labels for critical forms.

Example:

```html
<label class="pv-field">
  <span>Search keyword</span>
  <input type="search" placeholder="Search" />
  <button aria-label="Search"></button>
</label>
```

## Modal

Usage: settings, upload details, login, confirmations, menus requiring focus.

Visual structure:

- Acrylic background, `16px` blur, `6px` radius on desktop.
- Titlebar `48px` with title and close button.
- Content padding `24px` desktop, `16px` mobile.
- Footer with primary/secondary actions.

Token dependencies: `surface-acrylic`, `acrylic-blur`, `shadow-flyout`, `radius-md`, `transition-drawer`, `zIndex.menu`.

State rules:

- Enter desktop: fade and scale from `1.1`.
- Leave desktop: fade and scale to `.9`.
- Mobile: bottom-sheet slide from bottom.
- Focus: keep visible focus within modal.

Responsive rules:

- Desktop centered fixed modal.
- Mobile full-width bottom sheet.

Forbidden:

- Do not make modal content taller than viewport without scroll handling.
- Do not hide close affordance.

Example:

```text
Modal: titlebar, compact form, footer with cancel and primary save.
```

## Footer

Usage: landing pages, product pages, legal/community links.

Visual structure:

- Compact, light, low-contrast.
- Use muted link text and small accent separators or icon links.
- Optional pale geometry at edge.

Token dependencies: `background-light`, `icon-muted`, `accent-primary`, `space-4`, `space-6`.

State rules:

- Link hover turns accent.
- Focus ring must be visible.

Responsive rules:

- Desktop: short columns or inline groups.
- Mobile: stacked link groups with `44px` touch targets where actionable.

Forbidden:

- Do not use a large dark footer unless a brand adaptation explicitly requests it.

Example:

```text
Footer: product, community, docs, status, compact copyright.
```

