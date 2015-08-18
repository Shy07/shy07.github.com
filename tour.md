---
layout: page
title: Tour
---

<link rel="stylesheet" href="/stylesheets/ideal-image-slider.css">

<div id="slider">
  <img src="images/tour/t01.jpg" alt="tour 1" />
  <img data-src="images/tour/t02.jpg" src="" alt="tour 2" />
  <img data-src="images/tour/t03.jpg" src="" alt="tour 3" />
  <img data-src="images/tour/t04.jpg" src="" alt="tour 4" />
</div>

<script src="/javascripts/ideal-image-slider.js"></script>
<script>
  var slider = new IdealImageSlider.Slider('#slider');
  slider.start();
</script>