---
title: Bounce Forever
module: 11
jotted: true
---

# Bounce Forever

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Step1')">Step 1</button>
    <button class="tablinks" onclick="openTab(event, 'Step2')">Step 2</button>
    <button class="tablinks" onclick="openTab(event, 'Step3')">Step 3</button>
      <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

We made the circles come back from the right side, but what if we want them to continue forever?  We have to make the circle switch directions when it hits the left side.
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

What is the condition for which we want to check?  It should be when we are less than or equal to zero.  Why?  That is our left side.  What?!!
</div>
</div>
<div id="Step2" class="tabcontent">

<div class="tabhtml" markdown="1">

So, we could do what we did before.

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
    if(x <= 0)
    {
        movement *= -1;
    }
     x += movement;
}
```

Does it work?  Yeah!  Wait, though. Something feels a little off.  See how there is a duplicated section of code?  We don't want that.  How do we make that better?
</div>
</div>
<div id="Step3" class="tabcontent">

<div class="tabhtml" markdown="1">

We are going to introduce what is called **Logical Operators**.  
There are three of them, **AND**, **OR**, and **NOT**.  
In code, they look like this **&&** for AND, **||** for OR and <b>!</b> for NOT. 
Remember NOT?  
We did that earlier. Yes!

To combine the previous if statements, we have to think about this in English again.  When do we need movement to switch directions?  We can say if the circle is greater than or equal to 800 or if the circle is less than or equal to zero.  Wait!  Did you see the keyword?  **OR**.  Since we know what symbols to use, we can write the code above to look like this.

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
    if(x >= 800 || x <= 0)
    {
       movement *= -1;
    }

     x += movement;
}
```

Doesn't that make you feel better? It makes me feel better.  Now the duplicated code is gone.  We want to reduce duplicated code so that if we need to make a change, we only have to change it in one place.

If you look at the if statement with the OR symbol in it, only one of those conditions must be true.  When meeting one of the conditions, then movement is multiplied by -1.  If it's going to the right, it will be multiplied by -1 to make 13 become -13.  If it's moving to the left and we get to zero or below zero, multiplying negative one to movement causes the value to go from -13 to 13.  Pretty cool, right?

The circles should go back and forth forever.  If you want only the edge of the circles to hit the screen border, change the if statement.  Do you think you can figure that part out?  I think you can!

What math functions are out there that we can use?  Continue and find out!
</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/EuKB0GW3uPA" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="xxLXXPG" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/xxLXXPG">
  p5.js bounce forever</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>
