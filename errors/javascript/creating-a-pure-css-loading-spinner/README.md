# 🐞 Creating a Pure CSS Loading Spinner


This document details the creation of a loading spinner using only CSS.  No JavaScript is required.  This example utilizes CSS animations and transformations to create a visually appealing and performant loading effect.

**Description of the Styling:**

This spinner consists of four circular elements arranged in a square.  Each circle pulsates individually with a slight delay, creating a rotating effect. The styling uses keyframes to define the animation and transforms to rotate and scale the elements.  The overall effect is a clean and modern loading indicator.


**Full Code:**

```html
<!DOCTYPE html>
<html>
<head>
<title>CSS Loading Spinner</title>
<style>
.loader {
  width: 80px;
  height: 80px;
  position: relative;
  margin: 50px auto;
}
.loader div {
  position: absolute;
  width: 16px;
  height: 16px;
  background-color: #007bff;
  border-radius: 50%;
  animation: animate 1s linear infinite;
}
.loader div:nth-child(1) {
  top: 0;
  left: 0;
  animation-delay: 0s;
}
.loader div:nth-child(2) {
  top: 0;
  right: 0;
  animation-delay: 0.25s;
}
.loader div:nth-child(3) {
  bottom: 0;
  right: 0;
  animation-delay: 0.5s;
}
.loader div:nth-child(4) {
  bottom: 0;
  left: 0;
  animation-delay: 0.75s;
}
@keyframes animate {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.5);
    opacity: 0.5;
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}
</style>
</head>
<body>

<div class="loader">
  <div></div>
  <div></div>
  <div></div>
  <div></div>
</div>

</body>
</html>
```

**Explanation:**

* **`loader` class:** This container sets the size and positioning of the spinner.
* **`loader div`:**  This selects each of the four circular elements.  `position: absolute` allows precise placement.
* **`nth-child` selectors:** These target each circle individually to apply different animation delays.
* **`@keyframes animate`:** This defines the animation, scaling and fading each circle.
* **`animation-delay`:** This property creates the staggered effect of the animation.


**Links to Resources to Learn More:**

* **CSS Animations:** [MDN Web Docs - CSS Animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations)
* **CSS Transforms:** [MDN Web Docs - CSS Transforms](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)
* **CSS Selectors:** [MDN Web Docs - CSS Selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)


Copyrights (c) OpenRockets Open-source Network. Free to use, copy, share, edit or publish.

