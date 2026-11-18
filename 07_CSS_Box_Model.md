# 07 — CSS Box Model

Every element is represented as a rectangular box.

## Four parts

1. Content — text, image or other content.
2. Padding — space between content and border.
3. Border — line surrounding padding and content.
4. Margin — space outside the border.

## Example

```css
.box {
  width: 300px;
  padding: 20px;
  border: 5px solid black;
  margin: 15px;
}
```

With the default `content-box`, total rendered width is:

`300 + 20×2 + 5×2 = 350px` (margin excluded).

## box-sizing

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
```

With `border-box`, the declared width includes content, padding and border. This makes layout sizing easier to reason about.

## Margin and padding shorthand

```css
.card { margin: 10px 20px; }
.panel { padding: 10px 15px 20px 25px; }
```

Four-value order: top, right, bottom, left.

## Exercise

Create a 300px-wide card. Compare `content-box` and `border-box` by changing padding and border.
