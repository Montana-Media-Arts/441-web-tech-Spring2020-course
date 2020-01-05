---
title: Creating new Objects from Classes
module: 7
jotted: false
---

# Creating Objects from Classes

A lot of discussion has occurred about classes and objects, yet you still do not know how to formally create an object from your class definition!

To create a new object "of class type _X_", you need to call the `new` keyword, followed by the name of the class, including any constructor input parameters within parentheses trailing the class name. This can then be assigned to a variable for later reference.  Remember, we did this with the Array class.  It had the parentheses, but no parameters.

The following creates a new object, of class type `Person`, and passes it two input parameters. This new object is stored in the variable `myPerson`.

```js
let eyeColor = "blue";
let hairColor = "green";
let myPerson = new Person( eyeColor, hairColor );
```
<br/>
<iframe width="560" height="315" src="https://www.youtube.com/embed/gGc6NUT1Mnc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


# Accessing an Objects Properties

To access an objects properties, we will use the same "_dot notation_" as we learned about with objects data structures.

```js
myPerson.eyeColor; // ← returns the value of 'myPerson's eyeColor.
```

We can also set object properties using this same notation.

```js
myPerson.hairColor = "purple"; // ← sets the value of the property to purple
```

**NOTE:** Typically, when using classes and OOP paradigms, setting object properties with this notation is considered poor style. This is because it can lead to errors in code. More on this will be discussed later.

<iframe width="560" height="315" src="https://www.youtube.com/embed/r4mjFdaet5E" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Calling Object Methods

_dot notation_ is also used to execute object methods. However, parenthesis are always added to the method name, regardless of whether there are input parameters being passed to the method or not.

```js
myPerson.walk(); // ← executes myPerson's method, 'walk'.

myPerson.timeToTravel(distance); // ← execute the method and pass it one input parameter value.
```
<br/>
<iframe width="560" height="315" src="https://www.youtube.com/embed/q_wACy_hEGI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>