---
title: Add Shapes
module: 14
jotted: true
---

# Add a Cube

Although the black screen is appealing, let's add a shape to our scene.  The following code adds a cube.  Put it at the bottom of your script.

```js
var geometry = new THREE.BoxGeometry();
var material = new THREE.MeshBasicMaterial({
    color: 0x00ff00
});
var cube = new THREE.Mesh(geometry, material);
scene.add(cube);

camera.position.z = 5;
```

Save and take a look at your screen.  Do you see anything?  I don't either!  Dang!

So, how do we make it appear?  We need a little more code to make that happen. We need to animate the shape so that it will appear.

Add the following code under the last line.

```js
function animate() {
	requestAnimationFrame( animate );
	renderer.render( scene, camera );
}
animate();
```

Now, do you see something?  Like a green square?  Great!  Okay so that is fine, but the whole idea is that we want to see the power of threejs, just see a flat square.  So, above the render line, add these two lines.

```js
cube.rotation.x += 0.01;
cube.rotation.y += 0.01;
```

The final animate method should look like this.

```js
function animate() {
	requestAnimationFrame( animate );
    cube.rotation.x += 0.01;
    cube.rotation.y += 0.01;
	renderer.render( scene, camera );
}
animate();

```

Now, think about this for a second.  It's just rotating on it's own. That's pretty darn cool.  We didn't have to create a timer or use a jQuery function to animate this.  It is just animating because it's built into the library.  

What else can we do?  Move on and find out!