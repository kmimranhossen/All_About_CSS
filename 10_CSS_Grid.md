# 10 — CSS Grid

CSS Grid is a two-dimensional layout system for rows and columns.

## Create a grid

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}
```

## Responsive grid

```css
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 20px;
}
```

This allows columns to fit the available width while respecting a minimum card width.

## Define rows and areas

```css
.layout {
  display: grid;
  grid-template-columns: 220px 1fr;
  grid-template-areas:
    "sidebar header"
    "sidebar main";
  gap: 16px;
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
```

## Useful functions

- `repeat()` — repeats track definitions.
- `minmax()` — defines minimum and maximum track sizes.
- `fr` — fraction of available space.
- `gap` — spacing between tracks.

## Flexbox vs Grid

Use Flexbox for one-dimensional alignment; use Grid when managing rows and columns together. They can be combined.

## Exercise

Create a responsive gallery with at least six cards using CSS Grid.
