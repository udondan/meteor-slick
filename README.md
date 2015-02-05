
Slick
==========

Slick smart package for [Meteor][1].

Some features, as listed on the [demo page][2]:
* Fully responsive. Scales with its container
* Separate settings per breakpoint
* Uses CSS3 when available. Fully functional when not
* Swipe enabled. Or disabled, if you prefer
* Desktop mouse dragging
* Infinite looping
* Fully accessible with arrow key navigation
* Add, remove, filter & unfilter slides
* Autoplay, dots, arrows, callbacks, etc...

See [demo page][2] and [github project page][3] of the original Slick package for usage description and examples.

#Install
```sh
meteor add udondan:slick
```

#Minimal example
```html
<head>
  <title>Slick example</title>
</head>

<body>
  {{> carousel}}
</body>

<template name="carousel">  
  <div id="carousel">
    <div><img src="https://raw.githubusercontent.com/kenwheeler/slick/master/img/slick.gif" width="200px" /></div>
    <div><img src="https://raw.githubusercontent.com/kenwheeler/slick/master/img/slick.gif" width="200px" /></div>
    <div><img src="https://raw.githubusercontent.com/kenwheeler/slick/master/img/slick.gif" width="200px" /></div>
  </div>
</template>
```
```css
#carousel {
  border:   1px solid black;
  width:    200px;
  position: relative;
  top:      100px;
  left:     100px;
}

#carousel div {
  width:    200px;
}

.slick-prev:before, .slick-next:before {
  color:    silver;
}
```
```js
if (Meteor.isClient) {
  Template.carousel.rendered = function() {
    $('#carousel').slick({
      dots: true,
      arrows: true
    });
  }
}
```

  [1]: https://www.meteor.com/
  [2]: http://kenwheeler.github.io/slick/
  [3]: https://github.com/kenwheeler/slick/

#License
MIT, as the original Slick package
