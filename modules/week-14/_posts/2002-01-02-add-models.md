---
title: Add Models
module: 14
jotted: true
---

# Add Models

<a href="https://umontana.zoom.us/rec/play/7sd_Iu2vr2g3H9XH4gSDAPB_W43rJ_6s1HJI-vpcxRnnV3hWNgb0brJANzEfuQ5AF-kA6ZKNRv9XxzA?continueMode=true&_x_zm_rtaid=Jy8A7lfcT7a7lcNIPPwruA.1586580115012.04bd670198c0317137d387c683f84aae&_x_zm_rhtaid=860">Video Link</a>

threejs also allows you to add models that were created in other applications and exported as glb files.  The following example shows what is required to make the model appear.

```html
    <script src="js/three.js"></script>
    <script src="js/GLTFLoader.js"></script>
```
You need the threejs library of course, but you also need the GLTFLoader which is in the examples -> libraries folder as well.

```js
        var scene = new THREE.Scene()
        scene.overrideMaterial = new THREE.MeshBasicMaterial({
            color: 'green'
        });
        scene.background = new THREE.Color('grey');
        var camera = new THREE.PerspectiveCamera(45, window.innerWidth / window.innerHeight, .1, 1000)
        var renderer = new THREE.WebGLRenderer()
        camera.position.x = 100
        camera.position.y = -100
        camera.position.z = 590


        renderer.setClearColor(0xdddddd)
        renderer.setSize(window.innerWidth, window.innerHeight)

        document.body.appendChild(renderer.domElement)
        var loader = new THREE.GLTFLoader();

        // change to the name of your glb
        loader.load('CoolTrug.glb', function(gltf) {

            scene.add(gltf.scene);

        }, undefined, function(error) {

            console.error(error);

        });
        var rotation = 0

        function spinCamera() {
            rotation += 0.001
            camera.position.z = Math.sin(rotation) * 80;
            camera.position.x = Math.cos(rotation) * 80;
            camera.lookAt(scene.position)
        }
        var render = function() {

            requestAnimationFrame(render);
            spinCamera();

            renderer.render(scene, camera);
        };

        render();
```

Did you get to see your model?  Great!