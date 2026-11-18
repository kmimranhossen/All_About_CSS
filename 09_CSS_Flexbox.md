# 09 — CSS Flexbox

Flexbox is a one-dimensional layout system. It arranges items in a row or column.

## Enable Flexbox

```css
.container {
  display: flex;
}
```

## Main container properties

```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 16px;
}
```

- `flex-direction`: row, row-reverse, column, column-reverse.
- `justify-content`: alignment along the main axis.
- `align-items`: alignment along the cross axis.
- `flex-wrap`: whether items wrap.
- `gap`: space between items.

## Item properties

```css
.item {
  flex: 1 1 200px;
  align-self: stretch;
}
```

`flex` is shorthand for grow, shrink and basis.

## Center an element

```css
.parent {
  min-height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
}
```

## Exercise

Build a navigation bar with a logo on the left and links on the right. Make it wrap or adapt on narrow screens.
