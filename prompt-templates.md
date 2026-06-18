# Prompt Templates

Use these prompts as starting points. Replace bracketed fields with the user's product context.

## Official Homepage

```text
Use the Playful Video Platform UI skill to generate an original official homepage for [product/community name].

Inputs:
- page_type: homepage
- audience: [audience]
- content_domain: [domain]
- primary_goal: [goal]
- required_sections: app shell, banner hero, category/filter row, info bar, featured content grid, CTA band, compact footer
- brand_overrides: [accent/font/radius changes or none]
- responsive_targets: desktop, tablet, mobile
- accessibility_level: WCAG AA
- copy_tone: playful but clear

Output:
- Page structure
- Token mapping
- Component recipes used
- Desktop/tablet/mobile behavior
- Interaction states
- Accessibility notes
- Originality check
```

## Landing Page

```text
Use the Playful Video Platform UI skill to design a landing page for [product].

Make it light, pink-accented unless overridden, content-first, and not a clone of any source site. Use a banner hero with pale geometric decoration, concise CTA, feature cards, product/content preview grid, social proof or stats, and compact footer. Include responsive rules and interaction states.
```

## Product Introduction Section

```text
Use the Playful Video Platform UI skill to generate a product introduction section for [feature/product].

Include:
- Section heading with icon and optional badge
- 3 to 6 compact feature items
- One media or UI preview area
- Primary and secondary CTA
- Token mapping and component states
- Mobile stacking behavior
```

## Mobile Page

```text
Use the Playful Video Platform UI skill to create a mobile-first page for [task].

Constraints:
- Top appbar 56px
- Bottom nav 56px
- Content padding 16px
- One-column cards by default
- Touch targets at least 44px
- No horizontal overflow at 360px, 390px, or 430px
- Include focus, loading, and empty/error states
```

## Component Specification

```text
Use the Playful Video Platform UI skill to write a component specification for [component set].

For each component include:
- Usage
- Visual structure
- Token dependencies
- Hover, active, focus, disabled, loading/error states
- Desktop/tablet/mobile behavior
- Accessibility requirements
- Forbidden deviations
- Minimal implementation example
```

## Replace Color Style

```text
Use the Playful Video Platform UI skill and adapt the accent from warm pink to [new accent].

Preserve:
- Light canvas
- Slim app shell
- Small-radius cards
- Soft shadows
- Content-first grids
- Springy but short motion

Return the updated token mapping, affected components, contrast checks, and any tone changes.
```

## Replace Component Style

```text
Use the Playful Video Platform UI skill and adapt [component name] for [new product tone].

Keep the original interaction grammar and responsive behavior. Adjust only the allowed tokens and structural details from adaptation-rules.md. Explain which changes are observed-compatible and which are inferred.
```

