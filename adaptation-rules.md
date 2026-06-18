# Adaptation Rules

Use these rules when the user asks to change the tone, color, density, or component feel while preserving the distilled system.

## Replace The Primary Color

1. Choose one new accent color.
2. Generate hover, focus, pressed, soft, and faint ramps from that accent.
3. Keep the canvas white or near-white unless dark mode is explicitly requested.
4. Keep state colors independent from the accent unless the new brand requires a full semantic palette.
5. Validate contrast for text on accent and focus indicators.

Safe replaceable tokens:

- `accent-primary`
- `accent-hover`
- `accent-focus`
- `accent-pressed`
- `accent-soft`
- `accent-faint`
- `accent-ripple`
- `accent-shadow`

Do not replace:

- State colors without reason.
- Navigation structure.
- Card/content density.
- Motion scale.

## Replace Typography

Preserve two roles:

- Display font: expressive, geometric, high-weight, usable for headings and stats.
- Body font: legible, multilingual, strong UI readability.

Good substitutions:

- Display: Montserrat, Manrope, Sora, Outfit, Space Grotesk.
- Body: Inter, Pretendard, Noto Sans, system sans.

Avoid:

- Serif display as the primary tone unless making a premium adaptation.
- Script fonts.
- Fonts that cannot support the content language.

## Adjust Radius

- Default: `4px` controls and badges, `6px` cards and panels.
- Minimal adaptation: use `2px-4px`.
- Premium adaptation: use `6px-8px`.
- Friendly product adaptation: use `8px-10px`.
- Avoid large `16px-24px` card radii because they shift the style toward unrelated SaaS/card-heavy templates.

## Adjust Card Style

Light default:

- White/surface background.
- Soft shadow only where useful.
- No heavy border.
- `6px` radius.

More minimal:

- Reduce shadows.
- Add faint dividers.
- Keep hover/focus states.

More premium:

- Increase whitespace.
- Lower accent saturation.
- Use finer shadows.

More product-focused:

- Keep card recipes but add screenshot/mockup content.
- Add feature tags and compact CTA rows.

## Shift Tone

### Toward Premium

- Desaturate accent by 10-25 percent.
- Increase section spacing by one step.
- Reduce playful copy.
- Keep geometry but make it larger, paler, and less frequent.

### Toward Minimal

- Remove most decorative icons.
- Keep accent linework, active states, and focus rings.
- Use fewer shadows and more whitespace.
- Preserve small-radius components.

### Toward Corporate

- Replace playful wording with direct benefit statements.
- Use a blue, teal, or softened brand accent if requested.
- Reduce motion to default transitions and essential hover states.
- Keep app shell, component states, and responsive rules.

### Toward Product-Led

- Keep warm accent and community feel.
- Add product screenshots or original UI mockups.
- Use feature cards, stats, and CTA rows.
- Keep copy short and functional.

## Structure Rules Not To Replace

- The app-shell grammar.
- Compact content-first card hierarchy.
- Token-driven component states.
- Desktop/tablet/mobile breakpoint behavior.
- Mobile overflow safety.
- Originality and anti-copying checks.

## Consistency Validation After Adaptation

- Does the accent ramp remain coherent?
- Do primary, secondary, and tertiary controls still share one state grammar?
- Do cards still use small radii and soft elevation?
- Does mobile still use appbar/bottom nav or an equivalent compact shell?
- Is decoration still pale, geometric, and non-blocking?
- Are inferred changes labeled when not directly observed?

