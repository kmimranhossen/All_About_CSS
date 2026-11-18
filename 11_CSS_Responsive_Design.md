# 11 — CSS Responsive Design

Responsive design makes a page adapt to different screen sizes and devices.

## Viewport meta tag

Include this in the HTML `<head>`:

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

## Mobile-first CSS

Start with styles for smaller screens, then add enhancements for wider screens.

```css
.container {
  width: min(100% - 32px, 1100px);
  margin-inline: auto;
}

.cards {
  display: grid;
  grid-template-columns: 1fr;
  gap: 16px;
}

@media (min-width: 700px) {
  .cards {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1000px) {
  .cards {
    grid-template-columns: repeat(3, 1fr);
  }
}
```

## Flexible images

```css
img {
  max-width: 100%;
  height: auto;
}
```

## Useful responsive tools

- Media queries: `@media`
- Flexible layouts: Flexbox and Grid
- Relative units: `%`, `rem`, `vw`
- `min()`, `max()` and `clamp()`

## Breakpoint advice

Choose breakpoints when your content needs them rather than targeting specific device models.

## Exercise

Make a page with one column on mobile, two columns on tablet and three columns on desktop. Test by resizing the browser.
