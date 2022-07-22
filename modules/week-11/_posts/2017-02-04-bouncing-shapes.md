---
title: Bouncing Shapes
module: 11
jotted: true
---

# Bouncing Shapes

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Step1')">Step 1</button>
    <button class="tablinks" onclick="openTab(event, 'Step2')">Step 2</button>
    <button class="tablinks" onclick="openTab(event, 'Step3')">Step 3</button>
    <button class="tablinks" onclick="openTab(event, 'Step4')">Step 4</button>
    <button class="tablinks" onclick="openTab(event, 'Step5')">Step 5</button>
      <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

Now that you know how to make the shape stop, how to we make it go the opposite way when it hits the wall?
</div>
</div>
<div id="Step1" class="tabcontent">

<div class="tabhtml" markdown="1">

Let's start where we left off.

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
    if(x <= 800)
    {
        x+=13;
    }
}
```

The trick is that we need the x to go the opposite way.  How do we make the shape go to the left?  If adding to the x made it go to the right, then yes, subtracting makes it go to the left.  Remember, everything starts at 0,0 in the upper left-hand corner.  So, all we are doing is adding or subtracting to make this work.
</div>
</div>
<div id="Step2" class="tabcontent">

<div class="tabhtml" markdown="1">

So, what if we did this?

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
    if(x <= 800)
    {
        x+=13;
    }
    else
    {
        x-=13;
    }
}
```

Does this work?  What did you see?  Why did it just wiggle?  It actually did go back 13 pixels, but when the draw function runs again, it is less than or equal to 800, and then it tries to go to the right, and then it does this little dance over and over.  How can we make it work?
</div>
</div>
<div id="Step3" class="tabcontent">

<div class="tabhtml" markdown="1">

Instead of trying to add or subtract directly, what if we added all the time.  Let's not focus on adding, but rather, **what** we are adding.  We are going to make a couple of changes.  Check out this code.

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement = 13;
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
    if(x <= 800)
    {
       
    }
    
     x+=movement;
}
```

If you run this code, it will work just as did before, where the circles will continue forever.  Notice, I created a new variable **movement** and added that instead of 13.  What about the if statement?  
</div>
</div>
<div id="Step4" class="tabcontent">

<div class="tabhtml" markdown="1">


Here is where the magic is going to happen.

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement = 13;
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
    if(x >= 800)
    {
       movement*=-1;
    }
    
     x += movement;
}
```

Did you notice the changes?  I did two things.  I switched the direction of the relational operator from less than or equal to and made it "greater than or equal to."  The second thing I did was multiply movement by -1.  Why would I do that?  
</div>
</div>
<div id="Step5" class="tabcontent">

<div class="tabhtml" markdown="1">


Okay, let's break it down.

```js
    if(x >= 800)
    {

    }

    x += movement;
```

I changed the if statement so that the body only runs when x is equal to or beyond the right border.  What happens in there?  Now, the big reveal.

```js

    movement *= -1;

```

Multiplying movement by -1 is where the magic happens. After movement is multiplied by -1, the movement variable gets added back to the x variable.  However, now, movement is -7, and movement doesn't get multiplied by -1 again because x is not greater or equal to 800.

Cool right?  However, what about the other side?  Do you think you can do it?
</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/eRzFSvDH4nQ" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="ZEJXXJP" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/ZEJXXJP">
  p5.js bouncing</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>

