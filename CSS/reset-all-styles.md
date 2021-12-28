---
title: Reset all styles
tags: visual,beginner
firstSeen: 2018-02-28T21:51:36+02:00
lastUpdated: 2020-12-30T15:37:37+02:00
---

Resets all styles to default values using only one property.

- Use the `all` property to reset all styles (inherited or not) to their default values.
- **Note:** This will not affect `direction` and `unicode-bidi` properties.

```html
<div class="reset-all-styles">
  <h5>Title</h5>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure id
    exercitationem nulla qui repellat laborum vitae, molestias tempora velit
    natus. Quas, assumenda nisi. Quisquam enim qui iure, consequatur velit sit?
  </p>
</div>
```

```css
.reset-all-styles {
  all: initial;
}
```
