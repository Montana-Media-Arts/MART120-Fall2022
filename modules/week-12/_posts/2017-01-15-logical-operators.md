---
title: Logical Operators
module: 12
jotted: false
---

# Logical Operators

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'AND')">AND</button>
    <button class="tablinks" onclick="openTab(event, 'OR')">OR</button>
    <button class="tablinks" onclick="openTab(event, 'NOT')">NOT</button>
     <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
       <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>

</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

As we discussed last week, there are three logical operators - AND, OR, and NOT.  They are symbolized with **&&**, <b>||</b>, and <b>!</b>

</div>
</div>

<div id="AND" class="tabcontent">

<div class="tabhtml" markdown="1">

Let's look at the first operator AND

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

        if(x <= 200)
        {
            x+=10;
        } 
        else if(x > 200 && x <=300)
        {
            x+=2;
            console.log("second else if for x");
        }
        else if(x > 300)
        {
           x = 50;
        }
        
        if(y <= 200)
        {
            y+=3;
        }
          
        else if(y > 200 && y <= 300)
        {
            y+=1; 
            console.log("second else if for y");
        }
        else if(y > 300)
        {
            y = 50;
        }
        if(diameter <= 200)
        {
            diameter+=8;
        }
          
        else if(diameter > 200 && diameter <= 300)
        {
            diameter +=2;
            console.log("second else if for diameter");
        }
        else if(diameter > 300)
        {
            diameter = 25;
        }
        
    }
```

It wasn't doing what we wanted in the last section. It was only going into the first if statement and the final else if, but never the second. To make the code find the second else if, we need to make the changes above.  

For each second else if the variable must be higher than some number and if the same variable is less than some other number.  If the variables are greater than 200 and less than or equal to 300, then the variable will change at a different rate, and the console.log will print out.

Now, the variables change like before, but the changes slow down until it resets. Feel free to change the numbers.

</div>
</div>

<div id="OR" class="tabcontent">

<div class="tabhtml" markdown="1">

What do you think would happen if we changed it to an OR instead of an AND?  Let's find out.

Try this code out.

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

        if(x <= 200)
        {
            x+=10;
        } 
        else if(x > 200 || x <=300)
        {
            x+=2;
            console.log("second else if for x");
        }
        else if(x > 300)
        {
           x = 50;
        }
        
        if(y <= 200)
        {
            y+=3;
        }
          
        else if(y > 200 || y <= 300)
        {
            y+=1; 
            console.log("second else if for y");
        }
        else if(y > 300)
        {
            y = 50;
        }
        if(diameter <= 200)
        {
            diameter+=8;
        }
          
        else if(diameter > 200 || diameter <= 300)
        {
            diameter +=2;
            console.log("second else if for diameter");
        }
        else if(diameter > 300)
        {
            diameter = 25;
        }
        
    }
```

Why did it grow forever? Now that we inserted an OR, the x variable, for example, will change if it's higher than 200 or less than or equal to 300.  After meeting this condition, then variables grow forever.  These changes happen for the other two variables, y, and diameter too.

What needs to change so that all three if and else if's evaluate to true at some point?

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
        else if(x > 300)
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
        else if(y > 300)
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
        else if(diameter > 300)
        {
            diameter = 25;
        }
        
    }
```

</div>
</div>

<div id="NOT" class="tabcontent">

<div class="tabhtml" markdown="1">

So, what about NOT?  How does this fit in this scenario?

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

All we changed in this scenario is the last else if and as long x,y, or diameter isn't equal to their respective number, then the variable resets.

</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/bEsZJXSfq7U" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
<div id="ToDo" class="tabcontent">
<div class="tabhtml" markdown="1">

<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="vYJVqKp" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/vYJVqKp">
  p5.js Logical Operators</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>
</div>