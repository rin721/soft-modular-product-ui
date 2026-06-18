# Validation Checklist

Use this before delivering any UI, component spec, or generated code using this skill.

## Aesthetic Fit

- The result feels light, playful, content-first, and creator-community oriented.
- Warm accent or approved replacement organizes the interface.
- Decoration is pale, geometric, original, and non-blocking.
- The design avoids heavy dark gradients, oversized rounded cards, and stock-like generic hero treatment.

## Token Usage

- Colors map to `design-tokens.json`.
- Typography uses display/body roles correctly.
- Spacing follows the `4px` scale and specified container padding.
- Radii use `4px`, `6px`, pill, or circle unless adapted deliberately.
- Shadows are soft and tokenized.
- Motion uses documented durations and easing.

## Layout Grammar

- Desktop/tablet app shell uses `56px` left rail or a justified adaptation.
- Mobile uses top appbar plus bottom nav or a justified compact shell.
- Content grids follow media-card sizing rules.
- Sections are not wrapped in large decorative cards.
- CTA and footer are compact unless the user requested a landing-page expansion.

## Component Recipes

- Buttons include primary, secondary, tertiary/icon variants where needed.
- Navigation has active and focus states.
- Cards include media, title, metadata, and hover/focus behavior.
- Forms include focus, invalid, disabled, and loading behavior.
- Tags/badges use correct checked and count styles.
- Modals/flyouts use acrylic blur and responsive behavior.

## Interaction States

- Hover is defined for pointer devices.
- Active state reduces shadow and scales or compresses appropriately.
- Focus is visible and keyboard-friendly.
- Disabled state is visually and functionally disabled.
- Loading, empty, warning, success, and error states exist when relevant.
- Reduced motion fallback is specified for looping or large movement.

## Responsive

- Desktop, tablet, and mobile behavior is explicit.
- Mobile content has no horizontal overflow at `360px`, `390px`, and `430px`.
- Touch targets are at least `44px`.
- Text wraps or clamps safely.
- Decorative banners do not consume excessive mobile space.

## Accessibility

- Semantic HTML or roles are specified.
- Icon-only controls have accessible labels.
- Focus order follows visual order.
- Color is not the only active/error cue.
- Contrast is checked for accent buttons and text.
- Motion respects `prefers-reduced-motion`.

## Originality And Legal Boundary

- No source-site logo, wordmark, screenshots, video thumbnails, icons, or SVG paths are copied.
- No proprietary text, user names, video names, business data, or category dataset is copied as fixed content.
- Any mention of the source site appears only as evidence or origin context.
- Generated examples use fictional or generic product content.

## Agent Readiness

- Output is understandable without private tools.
- The result includes token mapping and component-state instructions.
- Inferred or unverified choices are labeled.
- The design can stand alone after removing all source-site context.

