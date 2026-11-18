# 14 — Advanced CSS Topics

## CSS custom properties

Custom properties (CSS variables) help reuse values.

```css
:root {
  --color-primary: #4f46e5;
  --space-md: 16px;
}

.button {
  background: var(--color-primary);
  padding: var(--space-md);
}
```

## `calc()`

```css
.content {
  width: calc(100% - 40px);
}
```

## `min()`, `max()` and `clamp()`

```css
.container { width: min(90%, 1200px); }
.sidebar { width: max(240px, 25%); }
h1 { font-size: clamp(2rem, 5vw, 4rem); }
```

## CSS nesting

Modern CSS supports nesting in current browsers:

```css
.card {
  padding: 20px;

  & h2 {
    margin-top: 0;
  }

  &:hover {
    transform: translateY(-2px);
  }
}
```

Check target browser support when using newer features.

## Cascade layers

```css
@layer reset, base, components;

@layer base {
  body { margin: 0; }
}

@layer components {
  .button { border-radius: 8px; }
}
```

## CSS organization tips

- Keep a consistent naming system.
- Use custom properties for repeated design tokens.
- Prefer simple selectors.
- Avoid unnecessary `!important`.
- Test keyboard focus and responsive behavior.
- Check browser compatibility for advanced features.

## Exercise

Create a small theme using CSS variables for primary color, background, text and spacing. Add a responsive heading using `clamp()`.
