---
title: OOP Terminology
module: 7
jotted: false
---


# OOP Terminology

Let me start by saying, there are a lot of terms.  Have you gathered that yet?  In programming, just like in your other classes, there are a lot of terms that we have to know in order to be successful.  I am one hundred percent sure, you all could start talking about some graphic design terms and I would be fairly lost.  However, once we learn the terms, then the subject matter becomes much less scary.

When it comes to OOP, there are two fundamental aspects.  They are Classes and Objects. 

Let's start again with **what**.  What are classes and and what are objects?

1. **Classes** - They are the blueprints or generic templates
2. **Objects** - They are the specific instances of those blueprints/templates.

Now that we know, the what, let's answer the better question **why**.

**Why do we use classes and objects**

We use classes to represent something in a generic way and specific objects to represent the actual items.

What does that mean?  Let's look at an example:

Let's take a person for an example.  What do all people have?

1. Eye Color
2. Number of Legs
3. Number of Arms
4. Hair Color
5. Height
6. Weight

That is our class.  If what I specified above is the generic template, then a specific instance or object is:

1. Blue eyes
2. 2 legs
3. 2 arms
4. Brown Hair
5. 5 foot 10 inches
6. 175 lbs

And we can create more people from the same class.  The nice part is that we don't have to create multiple classes, just multiple objects from the same class.

We will dig into Classes and Object in more detail in the next section.

<iframe width="560" height="315" src="https://www.youtube.com/embed/KpR0JqDM7l4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Property

An object or class **property** also known as an **attribute** is a piece of data used to describe the resulting object.

In our previous example, the properies were Eye color, Number of Legs, Number of Arms, Hair Color, Height, Weight.  All of these things described our person.

When we created the object, they all had values like Blue eyes, 2 legs, etc.

<iframe width="560" height="315" src="https://www.youtube.com/embed/ri_LeIl5YnQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Method

An object or class **method** is a function.  You can think of it as "It does stuff".  So, any function you create, which you have done already, just does stuff for you.

<iframe width="560" height="315" src="https://www.youtube.com/embed/AdjzvrJgjbw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Instantiation (aka. `new`)

When we create a new _object_ from a _class_, we are **instantiating** the _new_ object.

As we will see throughout this week's content, to create a new _instance_ of a class, we will use the JavaScript keyword `new`.

<iframe width="560" height="315" src="https://www.youtube.com/embed/ai-7VOugRNw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## this

A potentially confusing idea is the reference to "specific instances" of an object. When referring to a specific instance of an object, or, when referring to an object's own instance (from within the object) we will use the term **this**.

The `this` keyword in JavaScript is used throughout the language, and can be very confusing (hence why it has remained anonymous until now). Before we dive deep into `this`, just try and accept that `this` refers to a specific instance of an object from within that object itself.

<iframe width="560" height="315" src="https://www.youtube.com/embed/EhG17j2FmwM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>