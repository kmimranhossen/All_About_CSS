# All About CSS — Complete Beginner to Advanced Guide

**A practical CSS course for beginners**  
Level: Beginner → Advanced foundations  
Purpose: Learn to style responsive, accessible websites with CSS.

---

## How to use this guide

1. Learn the HTML structure first.
2. Create a folder named `All_About_CSS`.
3. Create `index.html` and `style.css`.
4. Link the stylesheet inside the HTML `<head>`:
   ```html
   <link rel="stylesheet" href="style.css">
   ```
5. Practise every example in your browser.
6. Use browser Developer Tools to inspect and debug styles.

CSS means **Cascading Style Sheets**. CSS controls how HTML content looks and how it is laid out.

## Contents

1. CSS introduction
2. Adding CSS to HTML
3. Selectors
4. Cascade, inheritance and specificity
5. Colours and backgrounds
6. Units and sizing
7. Box model
8. Typography and text
9. Borders, outlines and shadows
10. Display and visibility
11. Positioning and stacking
12. Flexbox
13. CSS Grid
14. Responsive design and media queries
15. Pseudo-classes and pseudo-elements
16. Transitions and transforms
17. Animations
18. CSS variables
19. Forms and UI styling
20. Accessibility and best practices
21. Debugging and browser tools
22. Complete practice projects
23. Exercises and quiz
24. Learning roadmap and resources

---

# 1. CSS introduction

CSS describes the presentation of an HTML document.

A CSS rule has a selector and a declaration block:

```css
p {
    color: navy;
    font-size: 18px;
}
```

- `p` is the selector.
- `color` and `font-size` are properties.
- `navy` and `18px` are values.
- Each property-value pair is a declaration.

HTML provides structure; CSS provides presentation.

# 2. Adding CSS to HTML

## External CSS (recommended)

`index.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Practice</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Hello CSS</h1>
    <p>My first styled page.</p>
</body>
</html>
```

`style.css`:

```css
body {
    font-family: Arial, sans-serif;
    background: #f4f6f8;
    color: #222;
}

h1 {
    color: #1769aa;
}
```

## Internal CSS

```html
<head>
    <style>
        h1 {
            color: tomato;
        }
    </style>
</head>
```

## Inline CSS

```html
<p style="color: green;">A paragraph</p>
```

Use external stylesheets for most projects because they are easier to maintain and reuse.

# 3. CSS selectors

Selectors choose the elements to style.

```css
/* Element selector */
p {
    color: #333;
}

/* Class selector */
.card {
    padding: 20px;
}

/* ID selector */
#main-title {
    color: darkblue;
}

/* Universal selector */
* {
    box-sizing: border-box;
}

/* Group selector */
h1, h2, h3 {
    font-family: Arial, sans-serif;
}

/* Descendant selector */
nav a {
    text-decoration: none;
}

/* Child selector */
.menu > li {
    list-style: none;
}

/* Attribute selector */
input[type="email"] {
    border: 1px solid #777;
}

/* Multiple classes */
.button.primary {
    background: royalblue;
}
```

Useful combinators:

- `A B`: descendant.
- `A > B`: direct child.
- `A + B`: immediately following sibling.
- `A ~ B`: later sibling.
- `[attribute]`: has an attribute.
- `[attribute="value"]`: attribute has an exact value.

# 4. Cascade, inheritance and specificity

The **cascade** decides which declarations apply when multiple rules target the same element.

Specificity is commonly described in this order:

1. Inline style.
2. ID selectors.
3. Class, attribute and pseudo-class selectors.
4. Element and pseudo-element selectors.

When specificity is equal, later applicable rules generally win. Origin, importance, cascade layers and scope can also affect the result.

```css
p {
    color: black;
}

.note {
    color: blue;
}

#warning {
    color: red;
}
```

```html
<p id="warning" class="note">This paragraph is red.</p>
```

Some properties, such as `color` and `font-family`, are inherited. Others, such as `margin` and `border`, are not normally inherited.

Avoid using `!important` as a routine fix. It makes future overrides harder.

# 5. Colours and backgrounds

CSS supports named colours, hex, RGB, HSL and newer colour formats.

```css
.example {
    color: tomato;
    background-color: #f0f4ff;
    border-color: rgb(20 80 150);
}

.overlay {
    background-color: rgb(0 0 0 / 50%);
}

.hero {
    background-image: url("images/hero.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}

.gradient {
    background: linear-gradient(120deg, #173b70, #35a6a0);
}
```

Check text/background contrast so content remains readable.

# 6. Units and sizing

Common CSS units:

- `px`: CSS pixels.
- `%`: relative to a relevant containing size.
- `em`: relative to the element's font size (or inherited font size in some properties).
- `rem`: relative to the root element's font size.
- `vw` / `vh`: viewport width / height.
- `dvh`: dynamic viewport height, useful on mobile.
- `fr`: a fraction of available space in CSS Grid.

```css
html {
    font-size: 16px;
}

.container {
    width: min(90%, 1100px);
    min-height: 50vh;
    padding: 2rem;
}

h1 {
    font-size: clamp(2rem, 5vw, 4rem);
}
```

Prefer flexible sizing over fixed widths for responsive layouts.

# 7. The CSS box model

Every element is represented by a rectangular box consisting of:

1. Content
2. Padding
3. Border
4. Margin

```css
*,
*::before,
*::after {
    box-sizing: border-box;
}

.card {
    width: 300px;
    padding: 20px;
    border: 2px solid #ccc;
    margin: 16px;
}
```

With `box-sizing: border-box`, the declared width includes padding and border. This is a common project-wide default.

# 8. Typography and text

```css
body {
    font-family: system-ui, Arial, sans-serif;
    font-size: 1rem;
    line-height: 1.6;
    color: #20242a;
}

h1 {
    font-size: clamp(2rem, 5vw, 3.5rem);
    line-height: 1.1;
    letter-spacing: -0.03em;
}

p {
    max-width: 70ch;
}

a {
    text-decoration-thickness: 0.08em;
    text-underline-offset: 0.2em;
}
```

Useful properties include `font-family`, `font-size`, `font-weight`, `font-style`, `line-height`, `letter-spacing`, `text-align`, `text-decoration`, `text-transform` and `white-space`.

# 9. Borders, outlines and shadows

```css
.panel {
    border: 1px solid #d8dee8;
    border-radius: 14px;
    box-shadow: 0 8px 24px rgb(0 0 0 / 8%);
}

button:focus-visible {
    outline: 3px solid #1769aa;
    outline-offset: 3px;
}
```

Use outlines for visible keyboard focus. Do not remove focus indicators without providing a clear replacement.

# 10. Display and visibility

Common display values:

- `block`: starts on a new line and generally takes available width.
- `inline`: flows with text; width and height do not behave like block boxes.
- `inline-block`: inline flow with box dimensions.
- `none`: removes the element from layout.
- `flex`: creates a flex formatting context.
- `grid`: creates a grid formatting context.

```css
.hidden {
    display: none;
}

.badge {
    display: inline-block;
    padding: 4px 10px;
}
```

`visibility: hidden` hides an element but keeps its layout space. `opacity: 0` makes it transparent but does not by itself remove it from interaction or accessibility trees.

# 11. Positioning and stacking

```css
.parent {
    position: relative;
}

.label {
    position: absolute;
    top: 12px;
    right: 12px;
}

.sticky-header {
    position: sticky;
    top: 0;
    z-index: 10;
}

.dialog-backdrop {
    position: fixed;
    inset: 0;
}
```

Position values:

- `static`: normal flow (default).
- `relative`: remains in flow and can be offset.
- `absolute`: positioned relative to a suitable positioned ancestor.
- `fixed`: positioned relative to the viewport in typical cases.
- `sticky`: behaves normally until a scroll threshold is reached.

`z-index` controls stacking within stacking contexts. A high value does not always place an element above everything because stacking contexts are independent.

# 12. Flexbox

Flexbox is useful for arranging items in one dimension: a row or a column.

```html
<div class="toolbar">
    <strong>My Site</strong>
    <nav>
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
    </nav>
</div>
```

```css
.toolbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
    flex-wrap: wrap;
}

.toolbar nav {
    display: flex;
    gap: 1rem;
}
```

Important container properties:

- `display: flex`
- `flex-direction`
- `justify-content`
- `align-items`
- `align-content`
- `flex-wrap`
- `gap`

Important item properties:

- `flex`
- `flex-grow`
- `flex-shrink`
- `flex-basis`
- `align-self`
- `order`

Use `gap` for spacing between flex items rather than adding unnecessary margins to every child.

# 13. CSS Grid

Grid is useful for two-dimensional layouts with rows and columns.

```html
<div class="cards">
    <article class="card">Card one</article>
    <article class="card">Card two</article>
    <article class="card">Card three</article>
</div>
```

```css
.cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1rem;
}

.card {
    padding: 1.5rem;
    border: 1px solid #ddd;
    border-radius: 12px;
}
```

Useful Grid properties:

- `grid-template-columns`
- `grid-template-rows`
- `grid-template-areas`
- `gap`
- `grid-column`
- `grid-row`
- `justify-items`
- `align-items`
- `place-items`

# 14. Responsive design and media queries

Responsive design makes a layout work across different screen sizes and input methods.

Start with flexible layouts, then add media queries when the design needs a change.

```css
.page {
    width: min(92%, 1100px);
    margin-inline: auto;
}

.layout {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 1.5rem;
}

@media (max-width: 700px) {
    .layout {
        grid-template-columns: 1fr;
    }
}
```

Other useful responsive tools:

```css
img {
    max-width: 100%;
    height: auto;
}

.title {
    font-size: clamp(1.8rem, 4vw, 3rem);
}

@media (prefers-reduced-motion: reduce) {
    *,
    *::before,
    *::after {
        scroll-behavior: auto !important;
        animation-duration: 0.01ms !important;
        transition-duration: 0.01ms !important;
    }
}
```

Do not target specific devices by name. Choose breakpoints where your content needs them.

# 15. Pseudo-classes and pseudo-elements

Pseudo-classes select an element in a particular state.

```css
a:hover {
    color: crimson;
}

button:focus-visible {
    outline: 3px solid royalblue;
}

input:invalid {
    border-color: crimson;
}

li:first-child {
    font-weight: bold;
}

.card:nth-child(even) {
    background: #f4f6f8;
}
```

Pseudo-elements style a particular part of an element or create generated content.

```css
.note::before {
    content: "Tip: ";
    font-weight: bold;
}

p::first-line {
    font-weight: 600;
}

::selection {
    background: #cce5ff;
}
```

Use generated content for decoration, not for essential information that must be available to assistive technology.

# 16. Transitions and transforms

Transitions animate changes between property values.

```css
.button {
    background: #1769aa;
    color: white;
    transition: background-color 180ms ease, transform 180ms ease;
}

.button:hover {
    background: #0d4e83;
    transform: translateY(-2px);
}
```

Common transform functions:

- `translate()`
- `scale()`
- `rotate()`
- `skew()`

Prefer animating `transform` and `opacity` for smooth effects. Respect reduced-motion preferences.

# 17. Animations

```css
@keyframes float {
    0%, 100% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(-10px);
    }
}

.floating-card {
    animation: float 3s ease-in-out infinite;
}

@media (prefers-reduced-motion: reduce) {
    .floating-card {
        animation: none;
    }
}
```

Animation properties include `animation-name`, `animation-duration`, `animation-timing-function`, `animation-delay`, `animation-iteration-count`, `animation-direction` and `animation-fill-mode`.

Avoid flashing effects and unnecessary continuous motion.

# 18. CSS custom properties (variables)

Custom properties store reusable values.

```css
:root {
    --color-primary: #1769aa;
    --color-text: #20242a;
    --space-md: 1rem;
    --radius-card: 14px;
}

.card {
    color: var(--color-text);
    padding: var(--space-md);
    border-radius: var(--radius-card);
    border: 1px solid var(--color-primary);
}
```

Custom properties can be overridden in a component or theme:

```css
.theme-dark {
    --color-text: #f5f7fa;
    --color-primary: #83c5ff;
}
```

# 19. Forms and UI styling

```css
input,
select,
textarea,
button {
    font: inherit;
}

.form-field {
    display: grid;
    gap: 0.4rem;
    margin-block: 1rem;
}

input,
textarea,
select {
    width: 100%;
    padding: 0.75rem;
    border: 1px solid #8993a2;
    border-radius: 8px;
}

button {
    padding: 0.75rem 1rem;
    border: 0;
    border-radius: 8px;
    background: #1769aa;
    color: white;
    cursor: pointer;
}

button:hover {
    background: #0d4e83;
}
```

Keep labels visible, focus states clear and error messages understandable. Do not rely only on colour to communicate validation state.

# 20. Accessibility and best practices

- Ensure text has sufficient contrast.
- Preserve visible keyboard focus.
- Do not remove browser zoom functionality.
- Support reduced-motion preferences.
- Use responsive layouts and readable text sizes.
- Avoid fixed heights for content that may wrap.
- Use semantic HTML; CSS cannot replace meaningful document structure.
- Do not communicate information through colour alone.
- Test keyboard navigation and mobile layouts.
- Keep styles organised and remove unused rules.

# 21. Debugging and browser tools

Use browser Developer Tools:

1. Right-click an element and choose Inspect.
2. Review the Styles panel.
3. Toggle declarations to test changes.
4. Check the Computed panel for final property values.
5. Inspect the box model.
6. Use the responsive device toolbar.
7. Check the Console for related errors.

Common problems:

- Wrong stylesheet path.
- Misspelled selector or property.
- Missing closing brace.
- A more specific selector overriding your rule.
- Browser cache showing an older stylesheet.
- Layout overflow caused by fixed widths or long content.

# 22. Complete practice projects

## Project 1: Profile card

Requirements:
- Card with image, name, role and short biography.
- Use padding, border radius and shadow.
- Add a responsive width.
- Include a visible hover and keyboard focus style for the link.

## Project 2: Responsive navigation

Requirements:
- Brand on the left and navigation links on the right.
- Use Flexbox.
- Allow wrapping on narrow screens.
- Maintain visible keyboard focus.

## Project 3: Responsive card gallery

Requirements:
- At least six cards.
- Use CSS Grid.
- Use `repeat()` and `minmax()`.
- Images should remain responsive.

## Project 4: Landing page

Requirements:
- Header, hero, feature cards and footer.
- Use CSS variables for colours and spacing.
- Use Grid and Flexbox where appropriate.
- Add one subtle transition.
- Test mobile and desktop layouts.

## Suggested folder structure

```text
All_About_CSS/
├── README.md
├── index.html
├── style.css
├── images/
└── projects/
    ├── profile-card/
    ├── responsive-navbar/
    ├── card-gallery/
    └── landing-page/
```

# 23. Exercises and quiz

### Exercises

1. Change the background and text colours of a page.
2. Create a reusable `.container` class.
3. Style headings with a responsive font size using `clamp()`.
4. Create a card using the box model.
5. Align a navigation bar with Flexbox.
6. Create a three-column card grid with CSS Grid.
7. Make the grid become one column on small screens.
8. Add hover and focus-visible states to buttons.
9. Create a dark theme using custom properties.
10. Add a reduced-motion media query.

### Mini quiz

1. What does CSS stand for?
2. Which selector selects a class?
3. Which property changes text colour?
4. Which property adds space inside an element's border?
5. Which layout system is designed for one-dimensional layouts?
6. Which layout system supports rows and columns?
7. What does `@media` do?
8. Which pseudo-class is useful for keyboard focus?
9. What does `box-sizing: border-box` change?
10. Which CSS feature stores reusable custom values?

### Answer key

1. Cascading Style Sheets.
2. `.class-name`
3. `color`
4. `padding`
5. Flexbox
6. CSS Grid
7. Applies styles when media or environment conditions match.
8. `:focus-visible`
9. Declared width and height include padding and border.
10. CSS custom properties (variables).

# 24. Learning roadmap and resources

Recommended order:

1. Selectors and declarations.
2. Cascade, inheritance and specificity.
3. Colours, units, typography and box model.
4. Display and positioning.
5. Flexbox and Grid.
6. Responsive design.
7. Pseudo-classes, transitions and animations.
8. Accessibility and debugging.
9. Build the four projects.
10. Learn JavaScript after becoming comfortable with HTML and CSS.

Free resources:

- [MDN CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [W3Schools CSS Tutorial](https://www.w3schools.com/css/)
- [web.dev Learn CSS](https://web.dev/learn/css/)
- [CSS-Tricks Almanac](https://css-tricks.com/almanac/)

## Completion checklist

- [ ] I understand CSS rules and selectors.
- [ ] I can explain the cascade and specificity.
- [ ] I understand the box model.
- [ ] I can use Flexbox and Grid.
- [ ] I can make a responsive layout.
- [ ] I can style forms and interactive states.
- [ ] I can use CSS variables.
- [ ] I can respect accessibility and reduced-motion preferences.
- [ ] I can debug CSS in browser Developer Tools.
- [ ] I have completed at least three projects.

---

**Keep experimenting. Inspect real websites. Build, test and improve.**
