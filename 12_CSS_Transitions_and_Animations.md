# 12 — CSS Transitions and Animations

## Transition

A transition animates a property change between states.

```css
.button {
  background: #4f46e5;
  color: white;
  transition: background-color 200ms ease, transform 200ms ease;
}

.button:hover {
  background: #3730a3;
  transform: translateY(-2px);
}
```

## Keyframe animation

```css
@keyframes fade-in {
  from { opacity: 0; }
  to { opacity: 1; }
}

.message {
  animation: fade-in 500ms ease both;
}
```

## Animation properties

- `animation-name`
- `animation-duration`
- `animation-timing-function`
- `animation-delay`
- `animation-iteration-count`
- `animation-direction`
- `animation-fill-mode`

## Respect reduced motion

```css
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

Avoid excessive motion and provide accessible experiences.

## Exercise

Create a button hover transition and a gentle fade-in animation for a card.
