---
title: Creating jQuery Plugins
module: 9
jotted: false
---

# Creating jQuery Plugins

How about if we want to make our own, though?  Even though it might sound daunting, it's not too bad.  Let's look at a small example:

```script
$.fn.bluey = function() {
    this.css( "background-color", "blue" );
};
```

We define the function with the `$.fn`, and then name it `bluey`.  Not sure if that is a word or not, but hey, why not?!

Then, the `function()` keyword creates the function, and the CSS applies the styles to whatever element uses the `bluey` function.

So, what does the whole page look like?

```html
<!DOCTYPE html>
<html>
<head>
    <script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
    <script>
        $.fn.bluey = function () {
            this.css("background-color", "blue");
        };

        $(function () {
            $("button").click(function () {
                $("#changeDiv").bluey();
            });

        });
    </script>
</head>
<body>
    <div id="changeDiv">Test information</div>
    <button id="btnSubmit">Click</button>
</body>
</html>

```

If you were to run this page, the background color of our div tag would turn blue when you click the button. Low and behold, we have a new look based on our function.  

<iframe width="560" height="315" src="https://www.youtube.com/embed/ammsnsb6Ngg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


We can have it apply to any tags we want.  And we can add more changes to the same jQuery plugin function.  It might look like this:

```html
<!DOCTYPE html>
<html>
<head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <script>
        $.fn.bluey = function () {
            this.css("background-color", "blue");
            this.css("color", "white");
            this.css("font-size", 24);
        };

        $(function () {
            $("button").click(function () {
                $("#changeDiv").bluey();
            });

        });
    </script>
</head>
<body>
    <div id="changeDiv">Test information</div>
    <button id="btnSubmit">Click</button>
</body>
</html>
```
<br/>
<iframe width="560" height="315" src="https://www.youtube.com/embed/97wPti2QG-s" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

For this to work in a chaining situation and survive in the real world, we must make some changes to the plugin.  First, we have to return `this`. This will return the object so that more functions can be chained to our plugin.  The function definition needs to be put into a **Immediately Invoked Function Expression** and then we need to pass the function jQuery so that it knows that it is a jQuery plugin and won't conflict with anything else.

The new fully qualified jQuery plugin looks like this now:

```script
    (function($){
        $.fn.bluey = function () {
            this.css("background-color", "blue");
            this.css("color", "white");
            this.css("font-size", 24);
            return this;
       };
    }(jQuery));
```

What this means is that we can do something like this now:

```html
<!DOCTYPE html>
<html>
<head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <script>
       
        (function($){
        $.fn.bluey = function () {
            this.css("background-color", "blue");
            this.css("color", "white");
            this.css("font-size", 24);
            return this;
        };
        }(jQuery));
        $(function () {
            $("button").click(function () {
                $("#changeDiv").bluey().fadeOut("slow").fadeIn("slow");
            });

        });
    </script>
</head>
<body>
    <div id="changeDiv">Test information</div>
    <button id="btnSubmit">Click</button>
</body>
</html>
```

At this point, you can create a simple jQuery plugin.  Come on, that's pretty cool!

<iframe width="560" height="315" src="https://www.youtube.com/embed/D-awHrt-Ves" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>