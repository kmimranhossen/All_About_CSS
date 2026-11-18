# 03 — CSS Syntax and Comments

## Basic syntax

```css
selector {
  property: value;
}
```

Example:

```css
p {
  color: #333;
  line-height: 1.6;
}
```

A selector identifies the HTML elements to style. A declaration block contains one or more declarations.

## CSS comments

Comments explain code and are ignored by the browser.

```css
/* This is a single-line CSS comment */

/*
  This is a
  multi-line comment
*/
```

## Multiple selectors

```css
h1,
h2,
h3 {
  font-family: Arial, sans-serif;
}
```

## Formatting tips

- Use consistent indentation.
- Put one declaration on each line.
- Add meaningful comments when they help.
- Group related rules together.
- Use readable class names.

## Practice

Write CSS rules for `body`, `h1`, `.container` and `.button`. Add a comment above each group.
