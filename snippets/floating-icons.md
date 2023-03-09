---
title: Floating icons
tags: animation
expertise: beginner
cover: image
firstSeen: 2023-03-09T05:00:00-04:00
---
Creates floating icons.

- Target `.icon` elements and set their `display` property to `inline-block`.
- Set the `animation` property of the `.icon` to `float`, with a duration of `3s`, an `ease-in-out` timing function, and an `infinite` repetition.
- Use `@keyframes` to define a three-step animation. At the start (0%) and end (100%), set the transform property to `translateY(0)`. In the 50% stage, set the transform property to `translateY(-10px)`.
- Target `.instagram` and `.twitter` to set their `animation-delay` property.
- Replace a, b, c with icons of your choice.

```html
<div>
  <i class="facebook icon">a</i>
  <i class="instagram icon">b</i>
  <i class="twitter icon">c</i>
</div>
```

```css
.icon {
  display: inline-block;
  font-size: 30px;
  animation: float 3s ease-in-out infinite;
}

.instagram {
  animation-delay: 1s;
}

.twitter {
  animation-delay: 2s;
}

@keyframes float {
  0%{
    transform: translateY(0);
  }
  50%{
    transform: translateY(-10px);
  }
  100%{
    transform: translateY(0);
  }
}
```