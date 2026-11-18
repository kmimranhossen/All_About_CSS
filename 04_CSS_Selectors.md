# 04 — CSS Selectors

Selectors target HTML elements.

## Common selectors

```css
/* Element selector */
p { color: #333; }

/* Class selector */
.highlight { background: yellow; }

/* ID selector */
#main-title { color: navy; }

/* Universal selector */
* { box-sizing: border-box; }

/* Group selector */
h1, h2, p { font-family: Arial, sans-serif; }
```

## Combinators

```css
/* Descendant: any p inside .card */
.card p { color: gray; }

/* Child: direct child paragraphs */
.card > p { margin: 0; }

/* Adjacent sibling */
h2 + p { font-weight: bold; }

/* General sibling */
h2 ~ p { color: teal; }
```

## Attribute selectors

```css
input[type="email"] {
  border: 1px solid blue;
}

a[target="_blank"] {
  text-decoration: underline;
}
```

## Specificity basics

When competing rules target the same element, specificity helps determine which rule wins. In general:

1. Inline styles
2. ID selectors
3. Class, attribute and pseudo-class selectors
4. Element and pseudo-element selectors

The cascade also considers origin, importance and source order. Avoid solving every conflict with `!important`.

## Exercise

Create a page with three paragraphs. Style one by element, one by class and one by ID. Test a descendant selector inside a card.
