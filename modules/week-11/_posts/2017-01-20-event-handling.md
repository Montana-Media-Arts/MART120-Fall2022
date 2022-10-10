---
title: Event Handling
module: 12
jotted: false
---

# Event Handling

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'KeyPressed')">keyPressed</button>
    <button class="tablinks" onclick="openTab(event, 'KeyIsDown')">keyIsDown</button>
    <button class="tablinks" onclick="openTab(event, 'Example')">Example</button>
     <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
       <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>

</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

So far, we transitioned our programs from static shapes to more movable shapes.  Now, we are going to make our shapes respond to events.

There are two events on which we will focus.  The first one is keyPressed.

</div>
</div>

<div id="KeyPressed" class="tabcontent">

<div class="tabhtml" markdown="1">

If we want to make changes to our program based on keys pressed, we must use a particular function called **keyPressed**.

Let's see how it works.

```js
var x = 100;
function setup()
{
    createCanvas(800,600);
}
function draw() 
{
  background(123,28,38);
  circle(x,100,50);
  
}
function keyPressed() 
{
  if (key == 'd') 
  {
    x+=15;
  } 
  else if (key == 'a') 
  {
    x-=15;
  }
}
```

The keyPressed function checks for the **d** key and then moves to the right, and then the **a** moves the circle to the left.
Notice something else?  The if/else if!  It's back and useful in this situation. If we didn't use the else if, it would be two if's, it would work the same, but the program would run just a little bit slower because it would have to check every if statement whereas with an else if, once one is true, the code ignores the others.

</div>
</div>

<div id="KeyIsDown" class="tabcontent">

<div class="tabhtml" markdown="1">

We have another option, though, too.  We can use the **keyIsDown** function also, and it looks like this.

```js
var x = 100;
function setup()
{
    createCanvas(800,600);
}
function draw() 
{
  background(123,28,38);
  if(keyIsDown(68))
  {
      x+=5;
  }
  if(keyIsDown(65))
  {
      x-=5;
  }
  circle(x,100,50);
}

```

You are probably thinking, umm.. what are those numbers doing in there?  Those are the key code numbers of the letters that we used in the keyPressed event.  So, **68** is **d** and **65** is **a**.  How did I find that out?  I used this code to figure them out.  You need to look at the console, but it will show it to you.

```js
function keyPressed() 
{
  console.log(key, ' ', keyCode);
  return false; // prevent default
}
```


Keep in mind that computers store all letters as numbers. That is why we can get the keyCode for each letter.

</div>
</div>

<div id="Example" class="tabcontent">

<div class="tabhtml" markdown="1">

How can we apply this to our example?  Let's look at what we had before.

```js
    var x = 50;
    var y = 50;
    var diameter = 25;
    function setup()
    {
        createCanvas(800,600);
    }
    function draw()
    {
        background(0);
        fill(24,200,29);
        circle(x,y,diameter);

        if(x <= 250)
        {
            x+=10;
        }
        else if(x == 250 || x <= 300)
        {
            x+=2;
            console.log("second else if for x");
        }
        else if(x != 300)
        {
           x = 50;
        }

      
        if(y <= 200)
        {
            y+=3;
        }

        else if(y == 250 || y <= 300)
        {
            y+=1; 
            console.log("second else if for y");
        }
        else if(y != 300)
        {
            y = 50;
        }
        if(diameter <= 200)
        {
            diameter+=8;
        }
          
        else if(diameter == 200 || diameter <= 300)
        {
            diameter +=2;
            console.log("second else if for diameter");
        }
        else if(diameter != 300)
        {
            diameter = 25;
        }
        
    }
```

Let's change this so that we can move our object with the **WASD** and have the circle increase continuously.  Let's look at how it evolved.

```js
    var x = 50;
    var y = 50;
    var diameter = 25;

    function setup() 
    {
      createCanvas(800, 600);
    }

    function draw() 
    {
      background(0);
      fill(24, 200, 29);
      circle(x, y, diameter);

      if (x >= 300) 
      {
        x = 50;
      }

      if (keyIsDown(83)) 
      {
        y += 10;
      } 
      else if (keyIsDown(87)) 
      {
        y -= 10;
      }

      if (y >= 300) 
      {
        y = 50;
      }

      if (diameter < 200) 
      {
        diameter += 2;
      } 
      else if (diameter >= 200) 
      {
        diameter = 25;
      }
    }

    function keyPressed() 
    {
      if (key == 'd') 
      {
        x += 10;
      } 
      else if (key == 'a') 
      {
        x -= 10;
      }
    }
```

Now, we are moving the object left and right while going up and down with the WASD keys, and then the diameter increases in size and then resets once the diameter reaches 200.

What else can we do?  Let's look at mouse events.

</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/kJyiKMFIKPI" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
<div id="ToDo" class="tabcontent">
<div class="tabhtml" markdown="1">

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="MWvPMbY" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/MWvPMbY">
  p5.js event handling</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>
</div>