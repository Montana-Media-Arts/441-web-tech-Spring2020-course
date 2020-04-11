---
title: Set up files
module: 14
jotted: true
---

# Set up

<a href="https://umontana.zoom.us/rec/play/tcEpdeiprWk3TIfDuQSDV_MrW42_Lf2s0SJM__cLyku0AiYFOgajYOEQZbEoWa68aZw9_HilB7JatnZJ?continueMode=true&_x_zm_rtaid=Jy8A7lfcT7a7lcNIPPwruA.1586580115012.04bd670198c0317137d387c683f84aae&_x_zm_rhtaid=860">Video Link</a>

The first thing we need to do is to make sure we have the correct setup.  Here is an example of a potential HTML file.

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>My first three.js app</title>
        <style>
            body { margin: 0; }
            canvas { display: block; }
        </style>
    </head>
    <body>
        <script src="js/three.js"></script>
        <script>
            // Our Javascript will go here.
        </script>
    </body>
</html>
```

Notice, the three.js file is in the js folder.  Just make sure you reference your folder.

There are three main parts to a threejs file. 

* scene
* camera
* renderer

I assume you have heard and used these terms before. Hopefully, this section won't be too much a stretch.  Here the beginning code.  The following code goes in your js file or between your script tags.  It's up to you.

```js
var scene = new THREE.Scene();
var camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.1, 1000 );

var renderer = new THREE.WebGLRenderer();
renderer.setSize( window.innerWidth, window.innerHeight );
document.body.appendChild( renderer.domElement );
```

The first line creates the scene by accessing the threejs library and then sets the camera. Then, the next instantiates the renderer.  Keep in mind; it must use WebGL to render anything in 3D, which is no different than p5 or processing if you remember from Creative Coding 1.  I bet you never thought that would come back!

If you run this, you should see a black screen. Not too exciting, is it?  

So, where do we go from here?