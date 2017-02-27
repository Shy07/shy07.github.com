---
layout: page
title: Tour de Mémoire
slider: true
signoff: true
---

<link href="/assets/css/ideal-image-slider.css" rel="stylesheet" type="text/css">

## PROLOGUE

<div id="slider">
  <img src="/images/tour/t04.jpg" alt="tour 1" />
  <img data-src="/images/tour/t01.jpg" src="" alt="tour 2" />
  <img data-src="/images/tour/t02.jpg" src="" alt="tour 3" />
  <img data-src="/images/tour/t03.jpg" src="" alt="tour 4" />
</div>

## GALLERY INFO.

|                   |                             |
|:------------------|:----------------------------|
|**Time**           |2014 Fall                    |
|**Place**          |Qingpu & Songjiang (Shanghai)|
|**Cycle**          |GIANT OCR3700                |

---

## Lost and found  
In a long time  
Rain is the tear of the god  
I thought  
Like a poet  

Several years’ losing  
Several years’ caring  
And one day  
We meet  

While the feeling became  
Clear and clear  
When nothing to talk  
Between the foes we are  
When the mailbox  
Become spider’s heaven  

I wake up  
I repent  
Time is just like a double-edged sword  
It gives me creativeness without hesitation  
While it wrested my social skills decidedly  

But why found must be after lost?  

Rain  
Necklaces made up by water drops I faced  
I just like a bird with injured wings  
Stay in the Phoenix Tree alone  

No interests to enjoy the beautiful scene  
One poem can’t express my helplessness  
Then how many can express?  
The answer may be made me more helplessness  

I came back our land again and again  
Waiting for the meeting unexpectedly  
But it be the cold rain again and again  

And one day
I try to ask the god  
Are you crying for me?  

No answer  
…  
Never answer  


<script src="/assets/js/ideal-image-slider.min.js"></script>
<script>
  var slider = new IdealImageSlider.Slider({
    selector: '#slider',
    height: $('#slider').width(),
    interval: 5000,
    effect: 'fade',
    disableNav: true,
  });
  slider.addBulletNav();
  slider.start();
  $(window).resize(function() {
    $('#slider').height($('#slider').width());
  });
</script>
