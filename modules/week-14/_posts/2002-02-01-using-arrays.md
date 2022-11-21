---
title: Work with Arrays
module: 15
jotted: true
---

# Working with Arrays

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Original')">Original Code</button>
    <button class="tablinks" onclick="openTab(event, 'Step1')">Step 1</button>
    <button class="tablinks" onclick="openTab(event, 'Step2')">Step 2</button>
    <button class="tablinks" onclick="openTab(event, 'Step3')">Step 3</button>
    <button class="tablinks" onclick="openTab(event, 'Step4')">Step 4</button>
    <button class="tablinks" onclick="openTab(event, 'Step5')">Step 5</button>
    <button class="tablinks" onclick="openTab(event, 'Step6')">Original Code</button>
    <button class="tablinks" onclick="openTab(event, 'Step7')">Code with Arrays</button>
    <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Original" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

Let's get hands-on with arrays now.  We will start with a simple example and then build on the model from last week.

```js
    var x = 50;
    var y = 50;
    var diameter = 25;
    var x1 = 150;
    var y1 = 150;
    var diameter1 = 125;

    function setup()
    {
        createCanvas(800,600);
    }

    function draw()
    {
        circle(x,y,diameter);
        circle(x1,y1,diameter1)
    }
```

Let's take this example and transform it to use arrays instead of multiple variables.

</div>
</div>
<div id="Step1" class="tabcontent">

<div class="tabhtml" markdown="1">

The code below shows how to implement this.

#### Declare the Arrays

```js
    var myXs = [];
    var myYs = [];
    var myDiameters = [];
```

#### Add values to the Arrays

```js
    function setup()
    {
        createCanvas(800,600);
        myXs[0] = 50;
        myYs[0] = 50;
        myDiameters[0] = 25;

        myXs[1] = 150;
        myYs[1] = 150;
        myDiameters[1] = 125;
    }
```

#### Use the values in the Arrays

```js
    function draw()
    {
        circle(myXs[0],myYs[0], myDiameters[0]);
        circle(myXs[1],myYs[1], myDiameters[1]);
    }
```

Let's talk about what is going on here.

In the first section, three arrays are created.  One to hold all the x values **myXs**, another to hold all the y values **myYs** and a third to hold all the diameter values **myDiameters**. 

Currently, they do not have any values in them, but they are identified as arrays because they have the **[]** after the equals sign.

**Note** As we explore arrays further, we can condense this even more, but for now, this will work for our purposes.

In the **setup** function, values are added to the arrays.  

When counting in arrays, the first slot always starts with the number 0.  The last number in the array is always the size of the array minus 1. Each one of these is called the **index** of an array.

So, in this instance, the first index is **myXs[0], myYs[0], myDiameters[0]**.  This means the first set of values into slot 0.

The second set of values are put into **myXs[1], myYs[1], myDiameters[1]**.
  
Where have started counting from zero before?  Yes, you are correct! for loops. We started with **var i = 0**.  That's because most languages start counting at zero instead of 1.

In the last section the two circles are created individually using the array indices that correspond to the index.  **The first circle uses the zero index** and **The second circle uses the one index**.

</div>
</div>

<div id="Step2" class="tabcontent">

<div class="tabhtml" markdown="1">

So, how can we change what we did before?

```js
    var myXs = [];
    var myYs = [];
    var myDiameters = [];

    function setup()
    {
        createCanvas(800,600);
        myXs[0] = 50;
        myYs[0] = 50;
        myDiameters[0] = 25;
        myXs[1] = 150;
        myYs[1] = 150;
        myDiameters[1] = 125;
    }

    function draw()
    {
        for(var i = 0; i < myXs.length; i++)
        {
            circle(myXs[i],myYs[i],myDiameters[i]);
        }
    }
```

Okay, only the draw changes in this iteration.  With the for loop each index is printed one by one using the array to print everything.  

This method allows one print multiple indices without having to change any code later.

The other thing to note is that **length** is used in the for loop instead of 2.  Length is a built-in property of the array and it returns how many items are in the array.  That way, if more items are added to the array, it still prints without having to change anything in the for loop. 

</div>
</div>
<div id="Step3" class="tabcontent">

<div class="tabhtml" markdown="1">

Let's make sure if we if add a third item, it still works.

```js
    var myXs = [];
    var myYs = [];
    var myDiameters = [];

    function setup()
    {
        createCanvas(800,600);
        
        myXs[0] = 50;
        myYs[0] = 50;
        myDiameters[0] = 25;
        myXs[1] = 150;
        myYs[1] = 150;
        myDiameters[1] = 125;
        myXs[2] = 250;
        myYs[2] = 250;
        myDiameters[2] = 75;

    }

    function draw()
    {
        for(var i = 0; i < myXs.length; i++)
        {
            circle(myXs[i],myYs[i],myDiameters[i]);
        }
    }
```

Did it work?  Yes!  However, there is one more thing we should address.  What about the number of circles that are created in the setup?  How do we make that better?

</div>
</div>
<div id="Step4" class="tabcontent">

<div class="tabhtml" markdown="1">


What if we create yet another for loop? Yes!

```js
    var myXs = [];
    var myYs = [];
    var myDiameters = [];

    function setup()
    {
        createCanvas(800,600);
        var x = 50;
        var y = 50;
        var diameter = 25;
        for(var i = 0; i < 3; i++)
        {
            myXs[i] = x;
            myYs[i] = y;
            myDiameters[i] = diameter;
            x += 50;
            y += 50;
            diameter += 25;
        }
    }

    function draw()
    {
        for(var i = 0; i < myXs.length; i++)
        {
            circle(myXs[i],myYs[i],myDiameters[i]);
        }
    }
```

Let's look at what we did.  We created a for loop in the setup.  This time, we went from 0 to 3.  We have to put in three because we do not have a length yet.  We also create three variables for the x,y, and diameter.  Then, we filled the three arrays. Each time through the for loop, we changed the x and y by 50 pixels and increased the size of the circle diameter by 25.  The best part, though, is that nothing in the draw had to change.

Automating stuff is pretty cool, but what if I wanted ten circles?

</div>
</div>
<div id="Step5" class="tabcontent">

<div class="tabhtml" markdown="1">

Look at this code and see what I had to change to do it.

```js
    var myXs = [];
    var myYs = [];
    var myDiameters = [];

    function setup()
    {
        createCanvas(800,600);
        var x = 50;
        var y = 50;
        var diameter = 25;
        for(var i = 0; i < 10; i++)
        {
            myXs[i] = x;
            myYs[i] = y;
            myDiameters[i] = diameter;
            x += 50;
            y += 50;
            diameter += 25;
        }
    }

    function draw()
    {
        for(var i = 0; i < myXs.length; i++)
        {
            circle(myXs[i],myYs[i],myDiameters[i]);
        }
    }
```

Guess what?  I only changed one thing.  The 3 in the for loop in setup is not a 10.  That was it!  Crazy!

</div>
</div>
<div id="Step6" class="tabcontent">

<div class="tabhtml" markdown="1">

How do we apply this to the project from last week? Let's start from where we left off.

```js

    var x = 50;
    var y = 50;
    var diameter = 25;
    var mousex = 0;
    var mousey = 0;
    var s = 83;
    var w = 87;
    var a = 65;
    var d = 68;

    function setup() 
    {
      createCanvas(800, 600);
    }

    function draw() 
    {
      background(0);
      
      fill(24, 200, 29);
      circle(x, y, diameter);

      // call the function created
      controlCircle();

      ellipse(mousex, mousey, 15, 50);

      // concentric circle where x = 110 and y = 120
      ConcentricCircle(110, 120, 100, 50, 50, 120, 120, 120, 50, 120);
      // concentric circle where x = 210 and y = 220
      ConcentricCircle(210, 220, 100, 50, 50, 120, 120, 120, 50, 120);
     
    }

    /* This function controls all the variables of the circle */
    function controlCircle()
    {
         if (x >= 300) 
      {
        x = 50;
      }
      
      if (y >= 300) 
      {
        y = 50;
      }

      if (keyIsDown(s)) 
      {
        y += 10;
      } 
      else if (keyIsDown(w)) 
      {
        y -= 10;
      }

      if (keyIsDown(d)) 
      {
        x += 10;
      } 
      else if (keyIsDown(a)) 
      {
        x -= 10;
      }
  
        // we call the function here.
        changeDiameter();

    }

    // This function updates the size of the circle
    function changeDiameter()
    {
        if (diameter < 200) 
        {
            diameter += 2;
        } 
        else if (diameter >= 200) 
        {
            diameter = 25;
        }

    }
    
    function mousePressed() 
    {  
      mousex = mouseX;
      mousey = mouseY;
    
    }

    // define ConcentricCircle function
    function ConcentricCircle(x,y, outer_diameter, inner_diameter, outer_red, outer_green,outer_blue, inner_red, inner_green, inner_blue)
{
        fill(outer_red,outer_green, outer_blue);
        circle(x,y,outer_diameter);
        fill(inner_red, inner_green, inner_blue);
        circle(x,y,inner_diameter);
}
```

When this runs, it should show the concentric circles, the player and placing a circle.  How can this be changed to use arrays?

</div>
</div>
<div id="Step7" class="tabcontent">

<div class="tabhtml" markdown="1">

Let's change the code from the previous step to the following.

```js
    var x = 50;
    var y = 50;
    var diameter = 25;
    var mousex = 0;
    var mousey = 0;
    var s = 83;
    var w = 87;
    var a = 65;
    var d = 68;

    var myXs = []; // create an array for the x coordinate
    var myYs = []; // create an array for the y coordinate
    var myDiameters = []; // create array for the diameter of circles

    function setup() 
    {
      createCanvas(800, 600);
      // create a for loop here to create the circles
        for(var i = 0; i < 2; i++)
        {
            // get all the random numbers to create a circles
            myXs[i] = getRandomNumber(800);
            myYs[i] = getRandomNumber(600);
            myDiameters[i] = getRandomNumber(100);
        }
    }

    function draw() 
    {
      background(0);
      
      fill(24, 200, 29);
      circle(x, y, diameter);

      // call the function created
      controlCircle();

      ellipse(mousex, mousey, 15, 50);

      for(var i = 0; i < myXs.length; i++)
      {
        // concentric circle randomly using arrays
        ConcentricCircle(myXs[i], myYs[i], myDiameters[i], myDiameters[i]/2, 50, 120, 120, 120, 50, 120);
      }
   }

    /* This function controls all the variables of the circle */
    function controlCircle()
    {
      if (x >= 300) 
      {
        x = 50;
      }
      
      if (y >= 300) 
      {
        y = 50;
      }

      if (keyIsDown(s)) 
      {
        y += 10;
      } 
      else if (keyIsDown(w)) 
      {
        y -= 10;
      }

      if (keyIsDown(d)) 
      {
        x += 10;
      } 
      else if (keyIsDown(a)) 
      {
        x -= 10;
      }
  
        // we call the function here.
        changeDiameter();

    }

    // This function updates the size of the circle
    function changeDiameter()
    {
        if (diameter < 200) 
        {
            diameter += 2;
        } 
        else if (diameter >= 200) 
        {
            diameter = 25;
        }

    }

    function mouseMoved() 
    {  
      mousex = mouseX;
      mousey = mouseY;
    
    }

    function getRandomNumber(number)
    {
        return Math.floor(Math.random()*number)+10;
    }

    // define ConcentricCircle function
    function ConcentricCircle(x,y, outer_diameter, inner_diameter, outer_red, outer_green,outer_blue, inner_red, inner_green, inner_blue)
    {
        fill(outer_red,outer_green, outer_blue);
        circle(x,y,outer_diameter);
        fill(inner_red, inner_green, inner_blue);
        circle(x,y,inner_diameter);
    }

```

There a few things to notice. First, I created a getRandomNumber function so I could create random locations and sizes of concentric circles  Then, I create a for loop to create the circle parameters and then print out the circles in the draw method using a for loop as well. Now, the concentric circles are not in the same place each time the page is run.

</div>
</div>
<div id="Video" class="tabcontent">
<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/zC-6jyGe-ck" frameborder="0" allowfullscreen></iframe></div>


</div>
</div>
<div id="ToDo" class="tabcontent" >
<div class="tabhtml" markdown="1">
<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="zYEObzo" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/zYEObzo">
  p5.js Array of Circles</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>
</div>
