---
title: Conditionals
module: 12
jotted: false
---


# Conditionals

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'IfExample')">if Example</button>
    <button class="tablinks" onclick="openTab(event, 'IfElseExample')">if/else Example</button>
    <button class="tablinks" onclick="openTab(event, 'IfElseIfExample')">if/else if Example</button>
     <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
     <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

These are control structures that help us make decisions when our code runs.

These are the most basic conditional statements.  They always evaluate to something true or false.

```js
    if(3 == 5)
    { // opening curly brace
        // body of the if statement
        console.log("I am in the if statement");
    }// closing curly brace
```



In these if statements, if 3 equals 5, then, the body of the if runs.  In this instance, the console.log will not run; however, if we change the if statement to something like this.


```js
    if(3 == 3)
    { // opening curly brace
        // body of the if statement
        console.log("I am in the if statement");
    }// closing curly brace
```

Then, the console.log runs.

Keep in mind; we want to use variables whenever we can.

You might want something like this.


```js
    if(a == b)
    { // opening curly brace
        // body of the if statement
        console.log("I am in the if statement");
    }// closing curly brace
```

Now, a could be three and b equal to 5. In that case, the if statement would fail, and then the code skips the body if statement and runs the code. However, if a = 3 and b = 3, then it evaluations to true.

</div>
</div>

<div id="IfExample" class="tabcontent">

<div class="tabhtml" markdown="1">
How do we apply this to our new example?

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
        if(x <= 300)
        {
            x+=10;
        }
        if(y <= 300)
        {
            y+=3;
        }
        if(diameter <= 300)
        {
            diameter+=8;
        }
        
    }
```

</div>
</div>

<div id="IfElseExample" class="tabcontent">

<div class="tabhtml" markdown="1">

We looked at this last week, and it's good to revisit before we add more.  With if statements, we can also have the other case.  We can think of it like this.  If something is true, then do something (the thing in the curly braces under the if); otherwise, do something **else** (it will have curly braces).
 
The syntax looks like this.

```js
    var a = 5;
    var b = 3;
    
    if(a == b)
    {
        console.log("a equals b");
    }
    else
    {
        console.log("a does not equal b");
    }
```

How did we do it in our project?

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
        if(x <= 300)
        {
            x+=10;
        }
        else
        {
            x-=20;
        }
        if(y <= 300)
        {
            y+=3;
        }
        else
        {
            y-=6;
        }
        if(diameter <= 300)
        {
            diameter+=8;
        }
        else
        {
            diameter-=16;
        }
        
    }
```

Remember this behavior?  It looks a little funky right? It was when we were trying to get our shape to bounce, and we just put in an else statement that said if we weren't higher than the width (or height), then subject.  That didn't work, so we had to create a new variable that would multiply by a negative one to speed and then add that to the shape.  

So, how can we effectively use an if/else statement?

What if we did something like this.

```js
    var a = 5;
    var b = 3;
    
    if(a == b)
    {
        console.log("a equals b");
    }
    else
    {
        console.log("a does not equal b");
    }
```

How did we do it in our project?

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
        if(x <= 300)
        {
            x+=10;
        }
        else
        {
            x = 50;
        }
        if(y <= 300)
        {
            y+=3;
        }
        else
        {
            y = 50;
        }
        if(diameter <= 300)
        {
            diameter+=8;
        }
        else
        {
            diameter = 25;
        }
        
    }
```

Now that's more interesting.  (or could cause a seizure depending your sensitivity).

</div>
</div>

<div id="IfElseIfExample" class="tabcontent">

<div class="tabhtml" markdown="1">
What about else if. What is that?


**else if** is just another way to check if a statement is true or false, and it makes things more efficient.  Take a look at the following code.

```js
    var a = 3;
    var b = 5;

if(a == b)
{
	console.log("a equals b");
}
else
{
	if(a > b)
	{
		console.log("a > b");
	}
	else
	{
		if(a < b)
		{
			console.log("a < b");
		}
	}
}
```

Yikes!  Do you see what I did here?  The previous code is what you must do if use just if/else. What should we do instead? Let's use an else if.  The syntax looks like this.

```js
    var a = 3;
    var b = 5;

    if(a == b)
    {
        console.log("a and b are the same");
    }
    else if(a < b)
    {
        console.log("a is less than b");
    }
    else if(a > b)
    {
        console.log("a is greater than b");
    }
```

 In the first, if statement, if true, all the others are skipped.  It continues in this fashion until there are no more **else if** statements.  Pretty cool, huh?  How do we apply it to our previous example?

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
        if(x <= 300)
        {
            x+=10;
        }
        else if(x > 300)
        {
            x = 50;
        }
        if(y <= 300)
        {
            y+=3;
        }
        else if(y > 300)
        {
            y = 50;
        }
        if(diameter <= 300)
        {
            diameter+=8;
        }
        else if(diameter > 300)
        {
            diameter = 25;
        }
        
    }
```

Okay, so maybe not that meaningful as it looks the same as the one from before.  However, what if we did this?

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
        if(x <= 300)
        {
            x+=10;
        }
        else if(x > 300)
        {
           x = 50;
        }  
        else if(x > 200 )
        {
            x+=5;
        }
        
        if(y <= 300)
        {
            y+=3;
        }
        else if(y > 300)
        {
            y = 50;
        }  
        else if(y > 200)
        {
            y+=1;
        }
        
        if(diameter <= 300)
        {
            diameter+=8;
        }
        else if(diameter > 300)
        {
            diameter = 25;
        }  
        else if(diameter > 200)
        {
            diameter +=4;
        }
        
        
    }
```

Do you think order matters?

What if we do this?

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
        if(x <= 300)
        {
            x+=10;
        }
        else if(x > 200 )
        {
            x+=5;
            console.log("second else if for x");
        }
        else if(x > 300)
        {
           x = 50;
        }  
       
        
        if(y <= 300)
        {
            y+=3;
        }
        else if(y > 200)
        {
            y+=1;
            console.log("second else if for y");
        }
        else if(y > 300)
        {
            y = 50;
        }  
        
        
        if(diameter <= 300)
        {
            diameter+=8;
        }
        else if(diameter > 200)
        {
            diameter +=4;
            console.log("second else if for diameter");
        }
        else if(diameter > 300)
        {
            diameter = 25;
        }  
        
    }

```

Now, did you see a change?  What happened?  Did it get to the third else if? How can we get it to work the way we want?

To make it work the way we want, we must change a couple of things.  Go to the next section to find out.

</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/drW6an-q51w" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
<div id="ToDo" class="tabcontent">
<div class="tabhtml" markdown="1">

<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="vYJVqGp" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/vYJVqGp">
  Untitled</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>
</div>