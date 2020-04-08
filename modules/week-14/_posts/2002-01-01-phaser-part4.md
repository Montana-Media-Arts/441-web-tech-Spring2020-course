---
title: Adding Text
module: 14
jotted: true
---

# Adding Text

One thing we want to be able to do is add text to our page as well. Adding 3D text is just another method call.

```js
var loader = new THREE.FontLoader();

loader.load( 'fonts/helvetiker_regular.typeface.json', function ( font ) {

	var geometry = new THREE.TextGeometry( 'Hello three.js!', {
		font: font,
		size: 80,
		height: 5,
		curveSegments: 12,
		bevelEnabled: true,
		bevelThickness: 10,
		bevelSize: 8,
		bevelOffset: 0,
		bevelSegments: 5
	} );
} );
```

Remember you need to add the fonts folder to your project for this to work.