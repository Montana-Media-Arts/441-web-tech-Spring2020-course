---
title: HTML5 Canvas
module: 11
jotted: true
---

# HTML5 Canvas

<iframe width="560" height="315" src="https://www.youtube.com/embed/ZwYFdU3lHSo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

The HTML5 Canvas is a revolutionary tag element that provides many benefits, such as:

* HTML Canvas Can be Animated
  * Canvas objects can move. Everything is possible: from simple bouncing balls to complex animations.

* HTML Canvas Can Be Interactive
  * Canvas can respond to JavaScript events.
  * Canvas can respond to any user action (key clicks, mouse clicks, button clicks, finger movement)

* HTML Canvas Used for Games
  * Canvas' methods for animations offer a lot of possibilities for HTML gaming applications.

Let's take a look at the most basic set up of the canvas.  If you want the canvas to appear, you need the canvas tag.  It looks like this:

```html
<html>
    <head>
        <title>Canvas</title>
    </head>
   
    <body>
        <canvas id="myCanvas" height="600" width="800"></canvas>

    </body>
</html>
```

#### Screenshot

![Example of Canvas](../imgs/canvas.png "Example of Canvas")

### Try it yourself!

How can you make a border around the canvas?  Use the code above to make a border so you can see the canvas outline.

<div id="jotted-demo-1" class="jotted-theme-stacked"></div>

<script>
    new Jotted(document.querySelector("#jotted-demo-1"), {
    files: [
        {
            type: "js",
            hide: false,
            url:"https://raw.githubusercontent.com/Montana-Media-Arts/441-WebTech-Spring2019/master/Week%2011%20Examples/handsonscript.js"
        },
        {
            type: "html",
            hide: false,
            url:"https://raw.githubusercontent.com/Montana-Media-Arts/441-WebTech-Spring2019/master/Week%2011%20Examples/HandsOnExample.html"

    }],
    showBlank: false,
    showResult: true,
    runScripts: true,
    plugins: [
        { name: 'ace', options: { "maxLines": 100, "Lines": 100 } },
        // { name: 'console', options: { autoClear: true } },
    ]
});
</script>

Did it work? Yes? Good job!

## How do we draw?

For us to interact with the canvas, we have to get the context of the canvas in 2d (3d requires a library and WebGL to help us).

```javascript
    var canvas = document.getElementById("myCanvas");
    var ctx = canvas.getContext("2d");   
```

Now, we can draw something by adding these two lines.  You should see a single blue square on your canvas.

```javascript
    ctx.fillStyle = "#0000FF";
    ctx.fillRect(50, 50, 10, 10);
```

### You give it a try!

<div id="jotted-demo-2" class="jotted-theme-stacked"></div>

<script>
    new Jotted(document.querySelector("#jotted-demo-2"), {
    files: [
        {
            type: "js",
            hide: false,
            url:"https://raw.githubusercontent.com/Montana-Media-Arts/441-WebTech-Spring2019/master/Week%2011%20Examples/handsonscript.js"
        },
        {
            type: "html",
            hide: false,
            url:"https://raw.githubusercontent.com/Montana-Media-Arts/441-WebTech-Spring2019/master/Week%2011%20Examples/HandsOnExample.html"

    }],
    showBlank: false,
    showResult: true,
    runScripts: true,
    plugins: [
        { name: 'ace', options: { "maxLines": 100, "Lines": 100 } },
        // { name: 'console', options: { autoClear: true } },
    ]
});
</script>

Did you get a little blue square? Yes? Great!

So, what else can we do?