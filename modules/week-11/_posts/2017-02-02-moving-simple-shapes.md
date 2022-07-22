---
title: Moving Simple Shapes
module: 11
jotted: true
---

# Moving Simple Shapes

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Example')">Initial Example</button>
    <button class="tablinks" onclick="openTab(event, 'Updated')">Updated Example</button>
    <button class="tablinks" onclick="openTab(event, 'Second')">Second Shape</button>
    <button class="tablinks" onclick="openTab(event, 'UpdatedSecond')">Updated Second Shape</button>
      <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

Remember, in the last section, how we created new variables and then used them to print out numbers and change colors?  What else can we do?  The better question is, why?

</div>
</div>

<div id="Example" class="tabcontent">

<div class="tabhtml" markdown="1">

Let's look at this example.

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;
 // this function is called only once
function setup()
{

    createCanvas(800,600);
}
/* this function is called continuously
    while the sketch is open in the browser
*/
function draw()
{
    background(redColor,greenColor,blueColor);
    circle(x,y,diameter);
}
```
Do you see your background with a circle?  I hope so!

All the background color variables are interesting, but you are probably saying, "How is this any different from before?";

</div>
</div>
<div id="Updated" class="tabcontent">

<div class="tabhtml" markdown="1">
Glad you asked!  Let's make a small change and see what happens.

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;
 // this function is called only once
function setup()
{

    createCanvas(800,600);
}
/* this function is called continuously
    while the sketch is open in the browser
*/
function draw()
{
    background(redColor,greenColor,blueColor);
    circle(x,y,diameter);
    x++;
}
```

Run the above code and see what happens.

Did the circle move?  Which way? Why?

What if we did the same to **y**?  Which way would it go?

</div>
</div>

<div id="Second" class="tabcontent">

<div class="tabhtml" markdown="1">

That is crazy!  We just made a simple shape move.  What if we added a second one?

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;
 // this function is called only once
function setup()
{

    createCanvas(800,600);
}
/* this function is called continuously
    while the sketch is open in the browser
*/
function draw()
{
    background(redColor,greenColor,blueColor);
    circle(x,y,diameter);
    circle(x,y,diameter);
    x++;
}
```

Do you get two circles?  Oh dang!  You don't.  You see only one.

</div>
</div>

<div id="UpdatedSecond" class="tabcontent">

<div class="tabhtml" markdown="1">

Well, technically, you do, but you only get to see one because the other one is on top of the first one because they are at the same x,y coordinate, and the same diameter. How can I prove it to you?  I know you are skeptics.

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;
 // this function is called only once
function setup()
{

    createCanvas(800,600);
}
/* this function is called continuously
   while the sketch is open in the browser
*/
function draw()
{
    background(redColor,greenColor,blueColor);
    fill(255);
    circle(x,y,diameter);
    fill(redColor,greenColor,blueColor);
    circle(x,y,25);
    x++;
}
```

What do you see?  I kept the second circle in the same location, reduced the size, and gave it a color - that is what the fill does.

There you go!  Okay, so if you let it run long enough, they should cruise right off the screen.  But what if we don't want that?  What if I say, make it so that it stops at the edge.  What are you doing to do?

Let's go to the next section and find out!

</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/FSAYViEEF9o" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="vYJeemy" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/vYJeemy">
  p5.js moving shapes</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

</div>