---
title: Canvas Classes
module: 12
jotted: true
---

# Class and Object Review

<iframe width="560" height="315" src="https://www.youtube.com/embed/hu9PQ4JYwzI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Recall, the implementation of Key Events use the following jQuery events.

```javascript
$(document).ready(function(){
    $(this).keypress(function(event){
        getKey(event);
    });
});

function getKey(event)
{
    var char = event.which || event.keyCode;
    var actualLetter = String.fromCharCode(char);
}
```

And we are back in this!  How do we create classes and objects again? Start with this.

```html
<html>
    <head>
        <title>Canvas</title>
         <style>
        #myCanvas{
            border:black;
            border-style: solid;
            border-width: 2px;
            
        }
    </style>
    </head>
   
    <body>
        <canvas id="myCanvas" height="600" width="800"></canvas>
        <script>
            var canvas = document.getElementById("myCanvas");
            var ctx = canvas.getContext("2d");
            var x = 50;
            var y = 50;
            ctx.fillStyle = "#0000FF";
            drawSquare();
            setInterval(update, 1000);

            function update()
            {
                
                drawSquare();
            }

            function drawSquare()
            {
                ctx.fillRect(x, y, 20, 20);
            }

        </script>
    </body>
</html>
```

Now, create a Square class and then use the fillRect above using the object you create.

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

Using your object and your key events, make sure you can update your object properties and move the square.  

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