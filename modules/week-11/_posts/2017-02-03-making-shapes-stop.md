---
title: Making Shapes Stop
module: 11
jotted: true
---

# Making Shapes Stop

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Step1')">Step 1</button>
    <button class="tablinks" onclick="openTab(event, 'Step2')">Step 2</button>
    <button class="tablinks" onclick="openTab(event, 'Step3')">Step 3</button>
    <button class="tablinks" onclick="openTab(event, 'Step4')">Step 4</button>
      <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

Last time, we left off with this.

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

Now, we have to make the shapes stop.  But how?
</div>
</div>
<div id="Step1" class="tabcontent">

<div class="tabhtml" markdown="1">
This where we come back to our **conditional** statements.

What was the one that we used the most in our math game? I hope you don't have bad dreams about that still.

If we think about it in English, we want the circles to move until we hit the right side of the wall.  Where is the right side of the screen border?  If we look at the createCanvas, it tells us.

It is the width.  Which one is that?  Is it the **800** or the **600**?

... It is the **800**, you are correct!

So, how does this look?

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
    if(x < 800)
    {
        x++;
    }
}
```

What happened above? I created an if statement and said if it is less than 800 than continue moving; otherwise, the if statement will be false, and the x will no longer get bigger.  If you want to make it go faster then, do this.  Keep in mind that **<** sign is called a relational operator. The opposite is **>** and stands for "greater than."
</div>
</div>

<div id="Step2" class="tabcontent">

<div class="tabhtml" markdown="1">
I could have done this, too, right?  Does this work? What are we doing? We use the **!** which means **NOT** equal in this case.

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
    if(x != 800)
    {
        x+=10;
    }
}
```

Run this.  Does it still work?  Why?  
</div>
</div>
<div id="Step3" class="tabcontent">

<div class="tabhtml" markdown="1">

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
    if(x != 800)
    {
        x+=13;
    }
}
```

How about now?  Why or why not? 
</div>
</div>
<div id="Step4" class="tabcontent">

<div class="tabhtml" markdown="1">

Remember, in the preceding if statement, it has to equal precisely 800 for it to stop. Otherwise, it will continue.  The **!=** is the equality operator, whereas the **==** is the equality operator and **=** is the assignment operator.  Be careful of those different operators!

But I do want the circle to move to the end. If the code remains strictly less than, then it won't get to the end of the screen.  Fixing this problem requires combining both the relational and equality operator together.  Now the symbols look like this **<=**.  The two symbols together mean "less than or equal to."  The opposite being **>=** or "greater than or equal to."

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
Now it works.  Whew!
</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/sWsHMGZ9Udg" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
<div id="ToDo" class="tabcontent">

<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="BadwwZJ" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/BadwwZJ">
  p5.js stop movement</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

</div>

