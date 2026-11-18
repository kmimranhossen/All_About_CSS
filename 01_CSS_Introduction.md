# 01 — Introduction to CSS

## What is CSS?

**English:** CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of HTML documents.

**বাংলা:** CSS হলো এমন একটি stylesheet language, যার মাধ্যমে HTML ওয়েবপেজের রং, ফন্ট, spacing, layout এবং responsive design নিয়ন্ত্রণ করা হয়।

## Why do we use CSS?

- Make web pages attractive.
- Control colors, fonts and spacing.
- Create layouts for different screen sizes.
- Add transitions and animations.
- Reuse styles across multiple pages.

## HTML vs CSS vs JavaScript

| Technology | Main responsibility |
|---|---|
| HTML | Structure / কাঠামো |
| CSS | Presentation / ডিজাইন |
| JavaScript | Behavior / কার্যকারিতা |

## Three ways to add CSS

### 1. Inline CSS

```html
<p style="color: blue;">Hello CSS</p>
```

### 2. Internal CSS

```html
<style>
  p {
    color: blue;
  }
</style>
```

### 3. External CSS

HTML:

```html
<link rel="stylesheet" href="style.css">
```

style.css:

```css
p {
  color: blue;
}
```

**Recommendation:** External CSS is generally best for maintainable projects.

## First practice

Create `index.html` and `style.css`. Add a heading, paragraph and button. Style each with a different color.

## Quick questions

1. What does CSS stand for?
2. Which technology creates the structure of a web page?
3. Which CSS method uses a separate `.css` file?
