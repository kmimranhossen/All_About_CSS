# 05 — CSS Colors and Backgrounds

## Color formats

```css
.box-name { color: tomato; }
.box-hex { color: #3366cc; }
.box-rgb { color: rgb(51, 102, 204); }
.box-hsl { color: hsl(220 60% 50%); }
.box-alpha { background: rgb(0 0 0 / 50%); }
```

Common formats include named colors, HEX, RGB, RGBA, HSL and HSLA.

## Background properties

```css
.hero {
  background-color: #eef4ff;
  background-image: url("hero.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
```

Shorthand:

```css
.hero {
  background: #eef4ff url("hero.jpg") center / cover no-repeat;
}
```

## Gradients

```css
.gradient {
  background: linear-gradient(120deg, #4f46e5, #06b6d4);
}

.sunset {
  background: radial-gradient(circle, #ffd166, #ef476f);
}
```

## Accessibility tip

Ensure sufficient contrast between text and its background. Do not communicate important information using color alone.

## Exercise

Create three cards: one with a solid background, one with a linear gradient and one with a background image.
