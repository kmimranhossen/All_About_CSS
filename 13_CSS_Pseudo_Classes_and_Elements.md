# 13 — Pseudo-classes and Pseudo-elements

## Pseudo-classes

A pseudo-class selects an element in a particular state.

```css
a:hover { color: crimson; }
button:focus-visible { outline: 3px solid orange; }
input:disabled { opacity: 0.5; }
li:first-child { font-weight: bold; }
li:nth-child(2n) { background: #f3f4f6; }
```

Common examples: `:hover`, `:focus`, `:focus-visible`, `:active`, `:checked`, `:disabled`, `:first-child`, `:last-child`, `:nth-child()`.

## Pseudo-elements

Pseudo-elements style a specific part of an element or create generated content.

```css
::selection {
  background: yellow;
  color: black;
}

p::first-letter {
  font-size: 2rem;
  font-weight: bold;
}

.required::after {
  content: " *";
  color: red;
}
```

Common examples: `::before`, `::after`, `::first-letter`, `::first-line`, `::selection`, `::placeholder`.

## Important note

For `::before` and `::after`, the `content` property is required for generated content to appear. Do not use generated content as the only place for essential information.

## Exercise

Style a button for hover, focus and active states. Add a decorative line before a section heading using `::before`.
