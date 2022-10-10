---
title: Mouse Events
module: 12
jotted: false
---

# Mouse Events

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'MousePressed')">mousePressed</button>
    <button class="tablinks" onclick="openTab(event, 'MouseClicked')">mouseClicked</button>
    <button class="tablinks" onclick="openTab(event, 'MouseMoved')">moveMoved</button>
     <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
       <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>

</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">
We can interact with our sketches using the mouse too. How do we do that?  We can use the **mousePressed** function to respond when pressing the mouse, and we can use the **mouseClicked** function, to respond when pressing and then releasing the moused.  We can also use the **mouseMoved()** function to respond to the mouse moving across the screen.

Let's look at mousePressed.

</div>
</div>

<div id="MousePressed" class="tabcontent">

<div class="tabhtml" markdown="1">

Starting with our previous code, we an integrate mousePressed like this.

```js
    var x = 50;
    var y = 50;
    var diameter = 25;
    var mousex = 0;
    var mousey = 0;
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

      circle(mousex, mousey, 30);
    }

    function mousePressed()
    {
        mousex = mouseX;
        mousey = mouseY;
        
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

Now a circle is drawn whenever we click the mouse.  It appears right when we click the mouse.

</div>
</div>
<div id="MouseClicked" class="tabcontent">

<div class="tabhtml" markdown="1">

What about the mouseClick function?

```js
    var x = 50;
    var y = 50;
    var diameter = 25;
    var mousex = 0;
    var mousey = 0;
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
      ellipse(mousex, mousey, 15, 50);
     
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

    function mouseClicked() 
    {  
      mousex = mouseX;
      mousey = mouseY;
    
    }

```

To test out the difference, you have to press down and then release the mouse.  Now, the ellipse draws to the screen.  

</div>
</div>

<div id="MouseMoved" class="tabcontent">

<div class="tabhtml" markdown="1">

What about the last one? mouseMove().

mouseMove tracks the mouse as it moves across the screen.

```js
    var x = 50;
    var y = 50;
    var diameter = 25;
    var mousex = 0;
    var mousey = 0;
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
      ellipse(mousex, mousey, 15, 50);
     
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

    function mouseMoved() 
    {  
      mousex = mouseX;
      mousey = mouseY;
    
    }

```

Now, you see the ellipse move with the mouse.  Pretty cool, right?  

</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/dXzwA0PYSD4" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
<div id="ToDo" class="tabcontent">
<div class="tabhtml" markdown="1">

<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="jOLejVj" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/jOLejVj">
  p5.js mouseMoved</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>
</div>