# Example: Landing Page

## Input Requirement

Create a landing page for a browser-based creator review tool. Audience: independent video creators. Primary goal: start a free trial. Tone: playful, clear, product-led.

## Skill Rules Used

- Aesthetic profile: light canvas, warm accent, playful geometric decoration.
- Layout grammar: banner hero, feature cards, media preview grid, CTA band, compact footer.
- Tokens: accent primary, display font, `6px` cards, soft shadows, default motion.
- Components: Hero, Button, Card, Feature List, Tag/Badge, Footer.
- Responsive: desktop dense layout, tablet reduced grid, mobile one-column.

## Generation Strategy

Use the app-shell flavor only lightly: a compact top nav is acceptable for a landing page, but include the same visual rhythm through icon buttons, accent active state, and soft surfaces. Do not use any source-site logo, screenshots, or content.

## Structure Draft

1. Top nav: product text mark, docs link, community link, start button.
2. Hero: product name, concise value prop, primary CTA, secondary demo link, pale diagonal accent bars.
3. Feature section: four compact cards for review, comments, timeline markers, and share links.
4. Preview grid: three original UI mockup cards with 16:9 previews.
5. Info band: short community or beta note.
6. CTA band: one primary button and one secondary link.
7. Footer: product, resources, community, status.

## Token Notes

- Accent: `#f06e8e`.
- Headings: display stack, 40px desktop, 30px mobile.
- Cards: `6px` radius, soft card shadow only on hover or stat cards.
- Buttons: min-height `36px` desktop, `44px` mobile.
- Motion: hover lift `-6px`, active `scale(.9722)`.

## Quality Checks

- No copied logos, images, icons, or text.
- Mobile uses one-column cards and no horizontal overflow.
- CTA focus ring is visible.
- Decorative geometry does not cover content.
- Reduced motion fallback removes continuous decoration.

