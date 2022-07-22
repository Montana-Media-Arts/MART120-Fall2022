---
title: Variables
module: 11
jotted: true
---

# Variables

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Example')">Variable Example</button>
    <button class="tablinks" onclick="openTab(event, 'Display')">Display Variable</button>
    <button class="tablinks" onclick="openTab(event, 'Increment')">Increment Variables</button>
    <button class="tablinks" onclick="openTab(event, 'Scope')">Variable Scope</button>
    <button class="tablinks" onclick="openTab(event, 'Type')">Variable Types</button>
    <button class="tablinks" onclick="openTab(event, 'Final')">Final Result</button>
      <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

Wait a minute; we have already done this, right?  Yes! We did this in JavaScript.  Since p5.js is just a JavaScript library, we can create variables just the same.

</div>
</div>

<div id="Example" class="tabcontent">

<div class="tabhtml" markdown="1">
For example, p5.js variables might look like this.

```js
    var myFavoriteNumber = 42;
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
        background(120);
        console.log(myFavoriteNumber);
    }
```

What do you see?  Well, you won't see anything on the screen, but you will see the number in your console of the browser.

</div>
</div>

<div id="Display" class="tabcontent">

<div class="tabhtml" markdown="1">

What if we want to do something with our variables?  We can add to our variables like this.

```js
    var myFavoriteNumber = 42;
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
        background(120);
        myFavoriteNumber++;
        console.log(myFavoriteNumber);
    }
```

Did you notice the change to **myFavoriteNumber**?  It gets incremented by 1.  

</div>
</div>

<div id="Increment" class="tabcontent">

<div class="tabhtml" markdown="1">


It can be written like this too.

```js
    myFavoriteNumber = myFavoriteNumber + 1;
```

They both mean the same thing. First, the value of one gets added to the previous value of myFavoriteNumber, and then it is assigned back to myFavoriteNumber.  There are three ways in which we can do the same thing. Here are the different choices.

```js
    myFavoriteNumber++;
    myFavoriteNumber = myFavoriteNumber + 1;
    myFavoriteNumber += 1;
```

They all mean the same thing.  Keep in mind that **myFavoriteNumber++** only happens when incrementing by 1.  If you want to increase by another number, you can only use the latter two.

</div>
</div>

<div id="Scope" class="tabcontent">

<div class="tabhtml" markdown="1">

Another thing to notice is how I declare **var myFavoriteNumber** above the setup() function.  That means it can be seen in the setup and draw functions as well as any other methods that we might define.

Declaring a variable inside of a method looks like this.

```js
    
    function doSomething()
    {
        var myFavoriteColor = "blue";
    }
    
```

This variable, **var myFavoriteColor** can be seen only in the doSomething() function.

You can also declare variables in loops like this.

```js
    for(var i = 0; i < 5; i++)
    {
        console.log(i);
    }
```

What this means is that the variable **i** will exist in the for loop, but when it terminates, the variable goes away.

</div>
</div>

<div id="Type" class="tabcontent">

<div class="tabhtml" markdown="1">

Did you notice the difference between creating a variable like myFavoriteNumber compared to myFavoriteColor?  The first one contains a number while the second contains a string.  These differences are important to understand.  When declaring a number, you do not need double-quotes **""**. Conversely, if you declare a string, it needs to be in double-quotes.

```js
    var name = "John Cena";
    var age = 67;
```

</div>
</div>
<div id="Final" class="tabcontent">

<div class="tabhtml" markdown="1">
What would a variable look like in our main sketch?

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;
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
}
```

As you can see, the variables **redColor**, **greenColor**, and **blueColor** are **declared** at the top and then used in the **background** function in the draw function.  

If we change the variables in the draw function as we did earlier to our favorite number, we should see something exciting.  Try this sketch.

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;
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
    redColor++;
    greenColor++;
    blueColor++;
}
```

Did you see something change?  Cool huh?  Let's continue.

</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/slL9LVJH9Es" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
<div id="ToDo" class="tabcontent">

<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="gOxGGmR" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/gOxGGmR">
  p5.js variables</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>