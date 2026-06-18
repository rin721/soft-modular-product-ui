# Responsive Rules

## Breakpoints

- Desktop: `>991px`.
- Tablet: `640px-991px`.
- Mobile: `<=639px`.

These breakpoints are observed in CSS. Desktop minimum is inferred as the complement to `<=991px`.

## Container Width And Padding

- Desktop: `padding: 26px 5dvw`.
- Tablet: `padding: 24px`.
- Mobile: `padding: 16px`.
- App shell offsets: desktop/tablet reserve `56px` left; mobile reserves `56px` top and `56px` bottom.

## Desktop

Use when viewport is wider than `991px`.

- Fixed left rail `56px`.
- Optional top banner or page title region.
- Media grid: `repeat(auto-fill, minmax(226px, 1fr))`.
- Category cards: two columns.
- Search page: centered module around `560px` wide.
- Upload page: dropzone plus stat cards in a row.
- Video detail: large player first, metadata/action area below, author block to the side when space allows.

## Tablet

Use from `640px` to `991px`.

- Keep left rail `56px`.
- Reduce content padding to `24px`.
- Media grid should land around 3 columns at 768px.
- Category cards can remain two columns if text fits; otherwise use one column.
- Avoid complex right-side panels unless they fit naturally.

## Mobile

Use at `<=639px`.

- Replace desktop rail with top appbar `56px` and bottom nav `56px`.
- Hide desktop banner decoration if it consumes too much vertical space.
- Use content padding `16px`.
- Default to one-column cards.
- A two-column media grid is allowed only if the card min width, text wrapping, and total container width prove no horizontal overflow.
- Keep bottom nav labels short and readable.
- Touch targets: `44px` minimum, `48px` preferred for nav icons.

## Grid Changes

- Desktop media grid: `auto-fill minmax(226px, 1fr)`.
- Tablet media grid: about 3 columns.
- Mobile media grid: one column by default.
- List layout: one column at all widths.
- Tile layout: `auto-fill minmax(360px, 1fr)` desktop, one column mobile.

## Navigation Changes

- Desktop/tablet side rail: vertical icon stack, active side indicator, soft rail shadow.
- Mobile top appbar: compact brand/title, menu/profile actions.
- Mobile bottom nav: three to five primary destinations, active accent state.
- Drawer/offcanvas: when open, viewport can blur, round to `6px`, translate right, and scale down. Use this only if it does not harm accessibility.

## Typography Scaling

- Do not scale fonts with viewport width.
- Base UI text remains `14px`.
- Metadata remains `12px` when legible.
- Display headings can step down on mobile, usually from `40px` to `28px-32px`.
- Avoid negative letter spacing.

## Section Spacing

- Desktop section gaps: `32px-48px`.
- Tablet section gaps: `24px-40px`.
- Mobile section gaps: `20px-32px`.
- Keep card internals compact to preserve browseability.

## Mobile Overflow Rule

Observed source behavior showed a horizontal overflow risk on a 390px mobile screenshot. Generated UIs must improve this:

- Use `box-sizing: border-box`.
- Avoid grid columns that exceed available width.
- Prefer `minmax(0, 1fr)` inside mobile two-column grids.
- Clamp long words and titles.
- Test at `360px`, `390px`, and `430px`.
- No primary content may require horizontal scrolling unless it is an intentional chip carousel with visible affordance.

