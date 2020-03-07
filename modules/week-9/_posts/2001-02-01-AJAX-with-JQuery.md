---
title: AJAX with jQuery
module: 9
jotted: false
---

# AJAX with jQuery

The previous examples were a little more complicated, wouldn't you agree?  How does JQuery help us with that?

Let's look at an example:

```html
<!DOCTYPE html>
<html>

<head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <script>
        $(document).ready(function () {
            $("button").click(function () {
                $("#bikeInformation").load("bikeInfo.txt");
            });
        });
    </script>
</head>

<body>
    <div id="bikeInformation">Nothing yet</div>
    <button>Get Bike Information</button>
</body>

</html>
```
<br/>

<iframe width="560" height="315" src="https://www.youtube.com/embed/hX2sMTCjOxA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

The basic syntax of the JQuery AJAX call looks like this.

`$(selector).load(URL,data,callback);`

The previous code shows how we can access elements using the jQuery selector, load some data from a URL, send data parameters, which are optional, and then add an optional callback function when the load is complete.

So, we could do something like this:

```html
<!DOCTYPE html>
<html>

<head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <script>
        $(document).ready(function () {
            $("button").click(function () {
                $("#bikeInformation").load("bikeInfo.txt", fadeText);
            });
        });

        function fadeText()
        {
            $("#bikeInformation").fadeOut("slow").fadeIn("slow");
        }
    </script>
</head>

<body>
    <div id="bikeInformation"></div>
    <button>Get Bike Information</button>
</body>

</html>
```
Here we execute a function after the data is retrieved and displayed.  Cool eh?

There are even more jQuery functions that you can use, but I will refer you to W3Schools to check them out.
[W3Schools JQuery AJAX](https://www.w3schools.com/jquery/jquery_ref_ajax.asp)

<iframe width="560" height="315" src="https://www.youtube.com/embed/m57TJlG7J_g" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>