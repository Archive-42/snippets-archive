---
title: Button fill animation
tags: animation,beginner
firstSeen: 2020-10-08T20:48:11+03:00
lastUpdated: 2021-04-02T21:34:43+03:00
---

Creates a fill animation on hover.

- Set a `color` and `background` and use an appropriate `transition` to animate changes to the element.
- Use the `:hover` pseudo-class to change the `background` and `color` of the element when the user hovers over it.

```html
<button class="animated-fill-button">Submit</button>
```

```css
.animated-fill-button {
  padding: 20px;
  background: #fff;
  color: #000;
  border: 1px solid #000;
  cursor: pointer;
  transition: 0.3s all ease-in-out;
}

.animated-fill-button:hover {
  background: #000;
  color: #fff;
}
```
