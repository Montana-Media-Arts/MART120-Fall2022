---
title: Using Functions
module: 13
jotted: true
---

# Using Functions

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Example1')">Concentric Circle Example</button>
    <button class="tablinks" onclick="openTab(event, 'Example2')">Concentric Circle Function</button>
      <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

Recall that **setup** and **draw** are built-in functions and are called by p5.js without the programmer having the explicitly call the function.  What are some other built-in functions in p5.js?

* floor(number)
* random()
* isKeyDown(keycode)
* circle(x,y,diameter)
* square(x,y,side)
* point(x,y)
* line(x,y,x2,y2)
* rect(x,y,width,height)
* ellipse(x,y,width,height)
* triangle(x,y,x2,y2,x3,y3)

There are so many functions that have been used already? (see the previous section as to why)  

Recall that when a function is **defined**, it starts with keyword **function**, and the **body** (the part that performs the action) is in between the curly braces.

However, when calling a function, the **function name** is printed, and then the name is followed by **parentheses** with or without parameters depending on the definition.

In the prior built-in p5.js examples, all functions required numbers between the parentheses except Math.random().  For example, the circle function requires an x, y, and a diameter.  These are called **parameters**.  When you call the function, then you pass **arguments** into the functions.

</div>
</div>
<div id="Example1" class="tabcontent">

<div class="tabhtml" markdown="1">

In this example, let's create a more interesting function that displays a circle inside of another circle.  What might that look like?

The following show how to create these circles directly in the draw function.

```js
    function setup()
    {
        createCanvas(500,500);
    }
    function draw()
    {
        fill(50,120,120);
        circle(110,120,100);
        fill(120,50,120);
        circle(110,120,50);
    }
```

To make this work, it requires, two calls to the fill function and two to the circle function.  How would one create a function to create a concentric circle?

</div>
</div>
<div id="Example2" class="tabcontent">

<div class="tabhtml" markdown="1">

However, if a programmer wants to create concentric circles in different places on the canvas, they can **define** a ConcentricCircle function like the one below.

```js

function ConcentricCircle(x,y, outer_diameter, inner_diameter, outer_red, outer_green,outer_blue, inner_red, inner_green, inner_blue)
{
        fill(outer_red,outer_green, outer_blue);
        circle(x,y,outer_diameter);
        fill(inner_red, inner_green, inner_blue);
        circle(x,y,inner_diameter);
}

```
I can then **call** the `ConcentricCircle` function in the draw function like this.

```js
    function setup()
    {
        createCanvas(500,500);
    }
    function draw()
    {
        ConcentricCircle(110, 120, 100, 50, 50, 120, 120, 120, 50, 120);
    }
```

The **ConcentricCircle** function is **called** in the draw function.  Now, multiple concentric circles are created by calling the ConcentricCircle function many times in the draw function.  However, in this case, it generates a second concentric circle is drawn in the same location.

```js
    function setup()
    {
        createCanvas(500,500);
    }
    function draw()
    {
        // creates two Concentric Cirles in the same place
        ConcentricCircle(110, 120, 100, 50, 50, 120, 120, 120, 50, 120);
        ConcentricCircle(110, 120, 100, 50, 50, 120, 120, 120, 50, 120);
    }
```

However, if one sends in different x and y, then a second concentric circle is drawn in a different location.

```js
    function setup()
    {
        createCanvas(500,500);
    }
    function draw()
    {
        // concentric circle where x = 110 and y = 120
        ConcentricCircle(110, 120, 100, 50, 50, 120, 120, 120, 50, 120);
        // concentric circle where x = 210 and y = 220
        ConcentricCircle(210, 220, 100, 50, 50, 120, 120, 120, 50, 120);
    }

    function ConcentricCircle(x,y, outer_diameter, inner_diameter, outer_red, outer_green,outer_blue, inner_red, inner_green, inner_blue)
    {
        fill(outer_red,outer_green, outer_blue);
        circle(x,y,outer_diameter);
        fill(inner_red, inner_green, inner_blue);
        circle(x,y,inner_diameter);
    }
```

What if I wanted to create random circles in random locations? Can you do that?

**Hint** use random() to get move the location of the circles.

</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/A--Fv7u5yXs" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
<div id="ToDo" class="tabcontent" >
<div class="tabhtml" markdown="1">
<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="rNzqEVV" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/rNzqEVV">
  p5.js Concentric Circles</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>
</div>