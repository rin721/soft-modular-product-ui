# Layout Patterns

## Overall Page Framework

Use an app shell rather than a marketing-only layout.

- Desktop and tablet: fixed left rail, `56px` wide, full viewport height.
- Mobile: top appbar `56px` plus bottom nav `56px`.
- Content viewport: scrollable area with hidden or custom scrollbars.
- Main canvas: white, with optional pale fixed decoration.
- Container padding: desktop `26px 5dvw`, tablet `24px`, mobile `16px`.

Observed source: CSS layout rules and screenshots. Confidence: high.

## App Shell

Desktop shell:

- Left rail contains top icon cluster, center vertical brand/decorative mark, and bottom settings/profile action.
- Active nav item uses accent icon, pale accent background, and a small vertical indicator.
- Rail shadow is soft pink-accent shadow.

Mobile shell:

- Top appbar shows menu or compact brand text.
- Bottom nav holds three to five primary destinations.
- Active item uses accent color and a pale pill/circle background.
- Avoid cramming full category nav into the top appbar.

## Section Rhythm

- Keep section headings compact.
- Use a small icon plus title for subheaders.
- Use a badge for counts.
- Put section-level content directly on the canvas or in individual cards. Do not wrap entire sections in large floating cards.

Typical order for a media/community homepage:

1. App shell.
2. Decorative banner or compact brand/title band.
3. Category nav or filter row.
4. Announcement/info bar.
5. Latest/content grid.
6. Optional CTA/footer band.

## Hero Modes

### Banner Hero

Use for homepages or product pages.

- Full-width top banner inside the app shell.
- Large display text or product name.
- Pale pink diagonal bars, dots, line shapes, or oversized icon.
- Keep the bottom of the first content section visible on landing-style pages.

### Center Stage Hero

Use for search, onboarding, and empty states.

- Center the title or product mark.
- Place segmented controls below.
- Place a large input, CTA, or search field below controls.
- Leave large quiet space around the stage.

### Functional Hero

Use for upload, settings, or player pages.

- Put the functional component first.
- Use a title banner above it.
- Decorative visuals should frame, not compete with, the tool.

## Content Area Patterns

### Media Grid

- Use `grid-template-columns: repeat(auto-fill, minmax(226px, 1fr))` on desktop.
- Use `gap: 0` at grid level and card internal padding/margins to create rhythm.
- Each card uses 16:9 thumbnail, title, uploader/metadata, count, duration, and date.
- Card hover lifts the card and changes title color to accent.

### Category Cards

- Two columns on desktop.
- Each row card has icon, label, and right-aligned badge.
- Use soft shadow and `6px` radius.
- Collapse to one column on mobile.

### Search Stage

- Center a compact search module.
- Use segmented control for search mode.
- Use an inset text field with trailing search icon.
- Keep surrounding space empty except for subtle decoration.

### Upload And Stats

- Warning/info bar at top.
- Dropzone as the dominant functional area.
- Stat cards align beside the dropzone on desktop.
- Stack dropzone and stats on mobile.

### Video Detail

- Large media/player block first.
- Metadata below: title, counts, date, category, source type.
- Action row uses icon buttons.
- Author/follow block may sit right of metadata on desktop.
- Tabs for comments/info can sit below player or metadata.

## CTA Area

Observed CTA behavior is limited. Inferred rule:

- Use a slim, soft info band or small panel, not a huge marketing card.
- CTA copy should be concise.
- Use one primary accent button and one secondary link/button.
- Keep decoration pale and edge-positioned.

Confidence: medium, inferred.

## Footer Pattern

Observed footer coverage is limited. Inferred rule:

- Use a compact footer with muted links and small accent separators.
- Place it below content, not as a large dark footer unless the brand adaptation requires it.
- Include copyright, links, social/community links, and status if applicable.

Confidence: low, inferred.

## Common Page Templates

### Creator Community Homepage

- App shell.
- Banner hero with categories.
- Announcement/info bar.
- Latest grid.
- Featured categories or recommended collections.
- Compact footer.

### Product Landing Page

- App shell or simple top navigation.
- Banner hero with product name and CTA.
- Feature cards using media-card proportions or icon cards.
- Product section with screenshots or original mockups.
- CTA band.
- Compact footer.

### Search/Browse Page

- App shell.
- Center search stage.
- Filter tags or segmented controls.
- Result grid or empty state.
- Pagination if needed.

### Mobile Page

- Top appbar.
- Primary content.
- One-column cards by default.
- Bottom nav.
- Avoid horizontal scrolling unless the element is an intentional chip carousel.

