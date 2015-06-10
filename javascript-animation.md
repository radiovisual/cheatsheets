#Javascript Animation

### Check to see if the browser supports the canvas tag

```js
﻿if (document.createElement('canvas').getContext) {
    console.log("The canvas element is supported.")
};
```

### Nomalize requestAnimationFrame() across browsers

```js
if (!window.requestAnimationFrame) {
    window.requestAnimationFrame = (window.webkitRequestAnimationFrame ||
        window.mozRequestAnimationFrame ||
        window.oRequestAnimationFrame ||
        window.msRequestAnimationFrame ||
        function (callback) {
            return window.setTimeout(callback, 1000/60);
        });
}
```

### Capture events on your canvas element

Note: the third argument here `false` is passing in the default value for
`useCapture` to handle browsers that require this argument.

```js
﻿canvas.addEventListener('mousedown', function (event) {
    console.log("Mouse pressed on element!");
}, false);
```

Popular mouse events:

- ﻿mousedown
- mouseup
- click
- dblclick
- mousewheel
- mousemove
- mouseover
- mouseout
- ﻿mousedown

Popular Touch Events:

- touchstart
- touchend
- touchmove

Popular Keyboard Events:

- keydown
- keyup


###  Degrees and Radians

```js
﻿radians = degrees * Math.PI / 180
degrees = radians * 180 / Math.PI
```

### Get distance between two points

```js
var dx = point.x - mouse.x;
var dy = point.y - mouse.y;
var dist = Math.sqrt(dx * dx + dy * dy);
```

### Convert int to HEX

Use the `Number.toString()` method and supply 16 as the radiux:

```js
// Convert the number 16733683 to hex
var hex = (16733683).toString(16);
// "ff55f3"
```

### Extract color composites from HEX color value

```js
var color = parseInt('ff0000', 16); // red color (16711680)

var red = color >> 16 & 0xff; // 255
var green = color >> 8 & 0xff; // 0
var blue = color & 0xff; // 0
```

