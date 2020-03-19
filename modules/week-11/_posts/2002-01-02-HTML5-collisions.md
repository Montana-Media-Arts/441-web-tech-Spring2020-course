---
title: HTML5 Collisions
module: 11
jotted: true
---

# HTML5 Collisions

<iframe width="560" height="315" src="https://www.youtube.com/embed/oeTBJ3_05ms" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

With any game, you need to be able to handle collisions. We are going to use a simple box collider.  It checks the corners of the boxes to see if they are overlapping.  If they are, then it returns true, else it returns false.  Keep in mind, a collision can be more precise, but it takes more processing because of all the algorithm checks all the points of the shape.  Also, every move checks collision.

Here is our collision code:

```javascript
function hasCollided(object1, object2) {
    return !(
        ((object1.y + object1.height) < (object2.y)) ||
        (object1.y > (object2.y + object2.height)) ||
        ((object1.x + object1.width) < object2.x) ||
        (object1.x > (object2.x + object2.width))
    );
}
```

Now, wait a minute. You might have thought that objects were going away. But what if I told you that you could create an object out of each of your squares (assuming you have at least two).  Then, you can send your objects into this function, and it will check to see if you have collided or not.

## Try it out!

Do you remember how to create a class? Can you create a class called Square with the properties x, y, height, width, and color?  Then, create your constructor and getters and setters.

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

Check to see if everything is in your objects by writing to the console.  Did it work? Yes? Great job!


## Try it yourself!

Can you create two squares and add them to the screen? Make them different colors and different sizes. (I know you can!  The power is in you!).

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

## Try it yourself!

Now, can you make the one square move with the KeyEvents using WASD?  Yes, yes, you can!

<div id="jotted-demo-3" class="jotted-theme-stacked"></div>

<script>
    new Jotted(document.querySelector("#jotted-demo-3"), {
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

Look how far you have come!  I am so proud of you!

## Try it yourself!

Now, here comes the new stuff, check for collision.  You can use the code above and check the collision between your two squares each time the first square moves.  Just make sure that the first square can no longer move or have the first square move back a bit from the second square (like a bounce)if they collide or move. It's up to you!

<div id="jotted-demo-4" class="jotted-theme-stacked"></div>

<script>
    new Jotted(document.querySelector("#jotted-demo-4"), {
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


You did it!  I am proud of you! I knew you could do it!  Is there more?  Of course, there is, but we are going to wait until next week to do more.  Good job this week!
    