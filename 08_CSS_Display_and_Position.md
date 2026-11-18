# 08 — Display and Position

## Display values

- `block` — starts on a new line and generally takes available width.
- `inline` — flows within text; width and height do not behave like block boxes.
- `inline-block` — flows inline but accepts width and height.
- `none` — removes the element from layout.
- `flex` — creates a flex formatting context.
- `grid` — creates a grid formatting context.

```css
.block { display: block; }
.inline { display: inline; }
.inline-box { display: inline-block; }
.hidden { display: none; }
```

## Position values

```css
.static { position: static; }
.relative { position: relative; }
.absolute { position: absolute; }
.fixed { position: fixed; }
.sticky { position: sticky; top: 0; }
```

- `static`: normal flow; default.
- `relative`: remains in normal flow and can be offset.
- `absolute`: positioned relative to its nearest positioned ancestor.
- `fixed`: positioned relative to the viewport in typical cases.
- `sticky`: behaves like normal flow until its scroll threshold.

## Example: badge inside a card

```css
.card {
  position: relative;
  padding: 24px;
}

.badge {
  position: absolute;
  top: 12px;
  right: 12px;
}
```

## Stacking order

`z-index` controls stacking in applicable stacking contexts. A larger number does not always win globally because stacking contexts are independent.

## Exercise

Create a card with a small “NEW” badge in its top-right corner.
