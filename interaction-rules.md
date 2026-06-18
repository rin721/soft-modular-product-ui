# Interaction Rules

## Motion Character

Motion should feel quick, elastic, and soft. Use motion to confirm state changes, not to distract.

Observed default:

```css
transition: all .25s cubic-bezier(.19,1,.22,1),
  color .1s cubic-bezier(.19,1,.22,1),
  fill .1s cubic-bezier(.19,1,.22,1);
```

## Hover

- Primary buttons: accent-hover background and stronger soft shadow.
- Secondary buttons: transparent accent hover overlay.
- Tertiary/icon buttons: neutral hover overlay.
- Media cards: lift by `6px`, add blur/soft surface, title turns accent.
- Tags: soft shadow.
- Menu items: soft overlay and slight text/content shift.

Confidence: high from CSS and screenshots.

## Active / Pressed

- Buttons, cards, tabs, pagination, and segmented thumbs use `scale(.9722)` or close equivalent.
- Icon buttons may scale icon to `.9`.
- Remove or reduce shadow during press.
- Selected vertical menu item indicator may shrink while pressed.

Confidence: high from CSS.

## Focus

- Always show visible focus.
- Primary focus ring: `0 0 0 3px color-mix(in oklab, var(--accent-focus), transparent 50%)`.
- Neutral focus ring for tertiary controls: gray mix.
- Text fields use accent bottom stripe on focus.
- Cards and checkboxes may use larger halo focus, but keep it soft.

Confidence: high from CSS.

## Disabled

- Use muted gray or accent-disabled.
- Remove shadow.
- Suppress pointer events.
- Reduce opacity where helpful, especially in dark mode or form controls.

Confidence: high from CSS.

## Loading

- Use a top page progress bar for route loading.
- Use accent progress ring for indeterminate loading.
- Use 2-4px progress bars inside buttons or toasts when progress is compact.
- Provide text labels for long loading states.
- Use skeletons or blurred placeholders for media cards; do not copy source thumbnails.

Confidence: medium; progress CSS observed, full runtime behavior partially unverified.

## Error And Warning

- Error: red stripe, red icon/label, concise message.
- Warning: orange info bar or toast, white text if on solid color.
- Success: green toast or completed outline animation.
- Do not make the whole app red/orange/green; state colors should be local.

Confidence: high for state colors and toast styles.

## Scroll

- Content sits inside a scrollable viewport with native scrollbars hidden or custom soft scrollbars.
- Custom scrollbar thumb uses muted icon color and blur.
- On touch, scrollbars should be unobtrusive.
- Do not block normal page scroll unless an app-shell viewport requires it.

Confidence: high from CSS.

## Transitions

- Default: `0.25s cubic-bezier(.19,1,.22,1)`.
- Spring selection: `0.5s cubic-bezier(.175,.885,.32,1.275)`.
- Drawer/modal enter: about `0.6s cubic-bezier(.1,.9,.2,1)`.
- Modal quick leave: about `0.15s-0.2s`.
- Background image or major decoration fade: about `1s`.

## Micro-Interactions

- Side rail icons can jump in with staggered delays.
- Settings icon may rotate when pressed or active.
- Segment thumbs slide and clip selected text.
- Upload success can trace an outline then animate upload icon.
- Toast progress fills linearly.
- Decorative icons may rotate slowly only when they do not affect task flow.

## Reduced Motion

For `prefers-reduced-motion: reduce`:

- Disable looping decorative rotation.
- Disable checkbox resize animations and replace with instant checked state.
- Disable indeterminate spinner loops or replace with static icon plus text.
- Preserve focus, hover, and active state changes without large transforms.

## Accessibility Guardrails

- Do not rely on color alone; combine icon, text, indicator, or position.
- Maintain visible focus for keyboard users.
- Keep touch targets at least `44px`.
- Avoid motion that moves large parts of the viewport without user intent.
- Provide accessible labels for icon-only actions.

