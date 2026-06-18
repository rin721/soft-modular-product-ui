# Example: Mobile Page

## Input Requirement

Create a mobile page for browsing creator tutorials. Audience: mobile viewers. Primary goal: find and open a tutorial quickly.

## Skill Rules Used

- Responsive rules: mobile appbar, bottom nav, one-column cards, no overflow.
- Layout grammar: search/filter row, latest grid/list, compact metadata.
- Components: Navigation, Form, Card, Tag/Badge, Content/empty state.
- Interaction: touch target sizing, focus, loading, empty/error states.

## Generation Strategy

Design mobile first. Do not reuse the source site's observed two-column overflow behavior. Use a one-column list or safe card layout with full-width thumbnails.

## Structure Draft

1. Top appbar: menu button, compact product text, profile/search icon.
2. Search field: inset background, trailing icon, visible label.
3. Filter tags: horizontal scroll with visible affordance or wrapping chips.
4. Tutorial list: full-width 16:9 media cards, title, creator, duration, date.
5. Empty/loading state: progress ring or content-unavailable block.
6. Bottom nav: Home, Browse, Following, Library.

## Token Notes

- Appbar and bottom nav: `56px`.
- Content padding: `16px`.
- Touch targets: `44px` minimum, `48px` preferred.
- Card radius: `6px`.
- Metadata text: `12px`, wraps safely.

## Quality Checks

- No horizontal overflow at `360px`, `390px`, or `430px`.
- Appbar and bottom nav do not overlap content.
- Cards are keyboard and screen-reader reachable.
- Icon-only controls have labels.
- Loading and error states avoid motion-only cues.

