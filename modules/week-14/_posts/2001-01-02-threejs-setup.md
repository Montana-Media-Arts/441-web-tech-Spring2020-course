---
title: Set up files
module: 14
jotted: true
---

# Set up

First thing we need to do is make sure we have the correct set up.  Here is an example of what your code in your html file could look like.

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

My guess is that you have heard and used those terms before so hopefully that isn't too much of a stretch.  Here is what the beginning code looks like.  The following code goes in your js file or between your script tags.  It's up to you.

```js
var scene = new THREE.Scene();
var camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.1, 1000 );

var renderer = new THREE.WebGLRenderer();
renderer.setSize( window.innerWidth, window.innerHeight );
document.body.appendChild( renderer.domElement );
```

So, it creates the scene in the first line by calling it out of the threejs library, then the camera an dhtne the renderer.  Keep in mind, it must use WebGL to render 3D which is no different than p5 or processing if you remember from Creative Coding 1.  I bet you never thought that would come back!

If you run this, you should see a black screen. Not too exciting is it?  

So, where do we go from here?
