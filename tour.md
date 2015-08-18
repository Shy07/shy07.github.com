---
layout: page
title: Tour
---

<div id="slider">
  <img src="/images/tour/t01.jpg" alt="tour 1" />
  <img data-src="/images/tour/t02.jpg" src="" alt="tour 2" />
  <img data-src="/images/tour/t03.jpg" src="" alt="tour 3" />
  <img data-src="/images/tour/t04.jpg" src="" alt="tour 4" />
</div>


<link href="/stylesheets/ideal-image-slider.css" rel="stylesheet" type="text/css">
<script src="/javascripts/ideal-image-slider.min.js"></script>
<script>
  var slider = new IdealImageSlider.Slider({
    selector: '#slider',
    height: 646,
    interval: 5000,
    effect: 'fade',
    disableNav: true,
  });
  slider.addBulletNav();
  slider.start();
</script>