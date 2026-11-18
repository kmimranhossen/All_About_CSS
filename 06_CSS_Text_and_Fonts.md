# 06 — CSS Text and Fonts

## Text properties

```css
.article {
  color: #222;
  text-align: left;
  text-decoration: none;
  text-transform: none;
  line-height: 1.7;
  letter-spacing: 0.2px;
  word-spacing: 2px;
}
```

## Font properties

```css
.heading {
  font-family: Arial, sans-serif;
  font-size: 2rem;
  font-weight: 700;
  font-style: normal;
}
```

Common `font-weight` values: `400` normal, `700` bold. Variable fonts may support a wider range.

## Importing a web font

You can use a web font provider or host font files yourself. For example:

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap');

body {
  font-family: 'Inter', sans-serif;
}
```

For production, consider performance, licensing and privacy when choosing a font source.

## Responsive typography

```css
h1 {
  font-size: clamp(2rem, 5vw, 4rem);
}
```

`clamp()` sets a minimum, preferred and maximum size.

## Exercise

Design a blog article with a heading, subtitle and body text. Use readable line height and a comfortable content width.
