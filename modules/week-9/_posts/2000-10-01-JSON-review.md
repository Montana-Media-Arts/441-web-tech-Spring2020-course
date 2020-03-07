---
title: JSON Review
module: 9
jotted: true
---

# JSON Review

Before we look at how to access data using AJAX, we will review JSON. Recall JSON stands for JavaScript Object Notation.  This way, we can store data as an object.

Remember, JSON is a standardized method for storing and transporting unordered collections of data. Data storage is through a _name:value_ pairs or key:value pairs. Furthermore, the _values_ in JSON data can be;

- strings
- numbers
- booleans
- arrays
- or other nested JSON objects


<br />


JSON Objects, once in JavaScript (i.e., after being sent over from an API on a remote server), appear as JS objects. As such, they can be traversed and manipulated using standard JS object notation and techniques.

As an example, the following code creates a JS Object, which is also valid as JSON.

```js
let bike = {
    "manufacturer" : "Santa Cruz",
    "model" : "5010",
    "owner" : {
        "firstName" : "Bob",
        "lastName" : "Jones"
    },
    "sizes" : [
        "small",
        "medium",
        "large",
        "x-large"
    ]
}
```

Once this object is bound to the variable `bike`, we can navigate through it and access its unique values.

<iframe width="560" height="315" src="https://www.youtube.com/embed/KQMSfQr8GT4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

The following example creates the same object as above but also demonstrates how to access values within the object.

```html
<html>
    <head>
        <script>
            let bike = {
                "manufacturer" : "Santa Cruz",
                "model" : "5010",
                "owner" : {
                    "firstName" : "Bob",
                    "lastName" : "Jones"
                },
                "sizes" : [
                    "small",
                    "medium",
                    "large",
                    "x-large"
                ]
            }

            function showBikeInfo()
            {
                document.getElementById("bikeInformation").innerHTML = "Manufacturer: " + bike.manufacturer 
                + "<br>Model:" + bike.model + "<br>First Name:" + bike.owner.firstName + "<br>Last Name:" 
                + bike.owner.lastName + "<br>Sizes Available:<br>" +
                bike.sizes[0] + "<br>" + bike.sizes[1] + "<br>" + bike.sizes[2] + "<br>" + bike.sizes[3];
            }
        </script>
    </head>

    <body>
        <div id="bikeInformation"></div>
        <button id="btnSubmit" onclick="showBikeInfo();">Show Information</button>
    </body>
</html>
```
This shows us traditional JSON key/value pairs, as well as JSON inside of JSON and an array inside of JSON.  That is good stuff!

<iframe width="560" height="315" src="https://www.youtube.com/embed/ND9uNZIv9g8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

But that's not all!  What about if we were doing this in jQuery?  Could you do it?

Let's look at an example:

```html
<!DOCTYPE html>
<html>

<head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <script>
         let bike = {
                "manufacturer" : "Santa Cruz",
                "model" : "5010",
                "owner" : {
                    "firstName" : "Bob",
                    "lastName" : "Jones"
                },
                "sizes" : [
                    "small",
                    "medium",
                    "large",
                    "x-large"
                ]
            }
        
        $(function () {
            $("button").click(function () {
                showBikeInfo();
            });

        });
       
        function showBikeInfo()
            {
                $("#bikeInformation").html("Manufacturer: " + bike.manufacturer 
                + "<br>Model:" + bike.model + "<br>First Name:" + bike.owner.firstName + "<br>Last Name:" 
                + bike.owner.lastName + "<br>Sizes Available:<br>" +
                bike.sizes[0] + "<br>" + bike.sizes[1] + "<br>" + bike.sizes[2] + "<br>" + bike.sizes[3]);
            }
        </script>
    </head>

    <body>
        <div id="bikeInformation"></div>
        <button id="btnSubmit" onclick="showBikeInfo();">Show Information</button>
    </body>
</html>

```

Keep in mind that I used the `.html` function so that I could display the break tags correctly.  Otherwise, everything else was pretty much the same.  All this information is exciting! It's all coming together.  So, why do we review JSON?  Well, as we talked about before, it's a ubiquitous delivery method from many different sources so we can read information from databases and server-side pages because they will give information back to the client via JSON.  So, let's look at AJAX.

<iframe width="560" height="315" src="https://www.youtube.com/embed/485pJBoSrpg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>