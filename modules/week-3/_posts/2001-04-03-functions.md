---
title: Functions
module: 3
jotted: true
---

# Functions

**Video**
<div class="embed-responsive embed-responsive-16by9"><iframe width="560" height="315" src="https://www.youtube.com/embed/eLZjLu6yIgY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

Okay, so now let's take it a step further and create a function.  Now, do you all feel comfortable with functions also known as methods? 

If not, methods/functions are chunks of code that can be reused and usually perform only one thing.  This is important so we don't have to duplicate code every where.  We want to maximize reusability and minimize maintainability.  That should be your manta!

So, now let's create a function and use it.

Create a new file and called it functions.html.  Enter the following:

```html
<html>
    <head>
        <title>Accessing the DOM</title>
        <script>
            function doSomething()
            {
                window.alert("HI");
            }
        </script>
   
    </head>
    <body>
        <div id="changeme">I love functions</div>
    </body>
</html>
```

Now, when you open this page, nothing happens.  Check the console and you shouldn't see any errors.  So, what happened? Remember, how I said HTML pages start at the top and read down?  It still did that but the function is not executed because the function is never called.  So, for this to work, we need to do something like this:

```html
<html>
    <head>
        <title>Accessing the DOM</title>
        <script>
            function doSomething()
            {
                window.alert("HI");
            }
        </script>
   
    </head>
    <body>
        <div id="changeme">I love functions</div>
        <script>
            doSomething();
        </script>
    </body>
</html>
```

Did you see the annoying popup box?  Yes!  You have created your first one.  It won't be your last...

The final portion that you need to know is changing the window.alert to something that will print out on the screen.

In order to do this, you want to change

```html
 window.alert("HI");
```

to something like this

```html
document.write("HI");
```

Now, it should show up on the web page as opposed to a popup.  Keep in mind that you can add HTML tags in between the double quotes.

```html
document.write("<h1>HI</h1>");
```
