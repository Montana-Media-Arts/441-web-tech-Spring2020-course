---
title: HTML5 Audio and Video
module: 12
jotted: true
---

# Audio and Video

<iframe width="560" height="315" src="https://www.youtube.com/embed/pu0i31fMOpQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Two of the most exciting tags elements introduced in HTML5 is the `audio` and `video` tags.  This allows us to embed audio and video just as easily as when we integrated images into our sites.

For Audio, the syntax is like this:

```html
<html>
    <head>
        <title>Audio/Video</title>
    </head>
    <body>
        <audio id="song" src="https://montana-media-arts.github.io/web-tech-Spring2019/data/Brahms.mp3" controls="controls">
        </audio>
        <br>
    </body>
</html>
```

As you can see the audio tag sets the src of the song and then plays the song.  There is an attribute called **controls** which allow the basic controls to appear for the music player.

Similarly, the video controls works the same way.  The syntax looks like this:

```html
<html>
    <head>
        <title>Audio/Video</title>
    </head>
    <body>

        <video id="film" src="https://montana-media-arts.github.io/web-tech-Spring2019/modules/week-12/data/BOOM.mp4" type="video/mp4" controls="true">
        </video>

    </body>
</html>
```


### Try it yourself!

1. Can you add your own audio? 
2. Can you add your own video? Find a great meme and make it appear!

**Hint** Remember you need a fully qualified URL here for example: **https://montana-media-arts.github.io/web-tech-Spring2019/data/Brahms.mp3**

#### Screenshot

![Example of Audio](../imgs/audio.png "Example of Audio")

![Example of Video](../imgs/video.png "Example of Video")

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

Did it work? Yes? Well done!

## Change Source with Events

For audio it looks like this:

```javascript
    var audio = document.getElementById("song");
    audio.src="https://montana-media-arts.github.io/web-tech-Spring2019/modules/week-12/data/Schubert.mp3";
```

and for the video, it would like like this:

```javascript
    var film = document.getElementById("film");
    film.src="https://montana-media-arts.github.io/web-tech-Spring2019/modules/week-12/data/Cat.mp4";
```

So, if we put it all together now.  The html file would look like this:

```html
<html>
    <head>
        <title>Audio/Video</title>
        <script src="main.js"></script>
    </head>
    <body>

        <audio id="song" src="https://montana-media-arts.github.io/web-tech-Spring2019/modules/week-12/data/Brahms.mp3" controls="controls">
        </audio>
        <br>
        <video id="film" src="https://montana-media-arts.github.io/web-tech-Spring2019/modules/week-12/data/BOOM.mp4" type="video/mp4" controls="true">
        </video>

        <p></p>
        <button onclick="updateAudio();">Change Audio</button>

        <p></p>
        <button onclick="updateVideo();">Change Video</button>

    </body>
</html>
```

While the JavaScript file would look like this:

```javascript
function updateAudio()
{
    var audio = document.getElementById("song");
    audio.src="https://montana-media-arts.github.io/web-tech-Spring2019/modules/week-12/data/Schubert.mp3";
}

function updateVideo()
{
    var film = document.getElementById("film");
    film.src="https://montana-media-arts.github.io/web-tech-Spring2019/modules/week-12/data/Cat.mp4";
}
```

### Try it yourself!

1. Can you change your audio with JavaScript?
2. Can you change your video with JavaScript?

#### Screenshot

![Example of Change](../imgs/change.png "Example of Change")


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

Did you get it? Yes? Great work! Keep it up!

## Changes with jQuery

We can do the same thing in jQuery like this:

```javascript
$(document).ready(function(){
    $("#audiochange").click(function(){
        updateAudio();
    });

    $("#videochange").click(function(){
        updateVideo();
    });
});


function updateAudio()
{
    $("#song").attr("src", "https://montana-media-arts.github.io/web-tech-Spring2019/modules/week-12/data/Schubert.mp3"); 
}

function updateVideo()
{
    $("#film").attr("src", "https://montana-media-arts.github.io/web-tech-Spring2019/modules/week-12/data/Cat.mp4");
}

```

and the HTML file would look something like this:

```html
<html>
    <head>
        <title>Audio/Video</title>
        <script src="libs/jquery.min.js"></script>
        <script src="scripts/main.js"></script>
    </head>
    <body>

        <audio id="song" src="https://montana-media-arts.github.io/web-tech-Spring2019/modules/week-12/data/Brahms.mp3" controls="controls">
        </audio>
        <br>
        <video id="film" src="https://montana-media-arts.github.io/web-tech-Spring2019/modules/week-12/data/BOOM.mp4" type="video/mp4" controls="true">
        </video>

        <p></p>
        <button id="audiochange">Change Audio</button>

        <p></p>
        <button id="videochange">Change Video</button>

    </body>
</html>
```


### Try it yourself!

1. Can you change your audio with jQuery?
2. Can you change your video with jQuery?

#### Screenshot

![Example of Change](../imgs/change.png "Example of Change")

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

You got it again? Yes? Good job! I knew you could do it!

So, what about the canvas?