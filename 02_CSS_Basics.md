# 02 — CSS Basics

## CSS declaration

A CSS declaration is made of a property and a value.

```css
h1 {
  color: purple;
  font-size: 32px;
}
```

- `h1` — selector
- `color` — property
- `purple` — value
- `font-size: 32px;` — declaration

## Common CSS properties

```css
.card {
  color: #222;
  background-color: white;
  width: 300px;
  padding: 20px;
  margin: 16px;
  border: 1px solid #ddd;
  border-radius: 12px;
}
```

| Property | কাজ |
|---|---|
| `color` | লেখার রং |
| `background-color` | পেছনের রং |
| `width` / `height` | প্রস্থ / উচ্চতা |
| `margin` | বাইরের ফাঁকা জায়গা |
| `padding` | ভেতরের ফাঁকা জায়গা |
| `border` | বর্ডার |
| `border-radius` | কোণা গোল করা |

## CSS units

- `px` — fixed CSS pixel unit
- `%` — relative to a containing value
- `em` — relative to the element's font size
- `rem` — relative to the root font size
- `vw` — viewport width
- `vh` — viewport height

```css
html { font-size: 16px; }

h1 { font-size: 2rem; } /* 32px when root is 16px */
.container { width: 90%; }
```

## Exercise

1. Make a heading 36px.
2. Give a paragraph a gray color.
3. Create a 320px-wide card with 20px padding.
4. Set the card border radius to 10px.
