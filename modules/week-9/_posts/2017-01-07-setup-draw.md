---
title: Setup and Draw
module: 9
jotted: true
---

# Setup and Draw

These are the two main functions in p5.js.  They are the most critical functions and built into this library.

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Setup')">Setup</button>
    <button class="tablinks" onclick="openTab(event, 'Draw')">Draw</button>
    <button class="tablinks" onclick="openTab(event, 'FinalPage')">Final HTML Page</button>
     <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Setup" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

The **setup** function is the first function called and called only once.  createCanvas is another built-in function that sets up the main window that allows us to draw.

It looks like this.

```js
    createCanvas(300,500);
```

There are some essential things to notice. Hopefully, the look isn't too mysterious. **createCanvas** is the name of the function.  We know it's a function because of the **()** and the first **parameter**, **300** is the width, while the second parameter, **500**, is the height and then, don't forget the **;** semicolon.

**Note** Remember a parameter is something that passed into a function - some value.  The semicolon is needed to end the statement.

To make the canvas appear, add the createCanvas to the setup function.  It looks like this.

```js
    function setup()
    {
        createCanvas(300,500);
    }
```

Why do we put the createCanvas function in the setup? We only want to create the canvas one time.

Give this a try and look at the result.

Did you get a canvas to appear in your web browser? Good!

</div>
</div>
<div id="Draw" class="tabcontent">

<div class="tabhtml" markdown="1">

What about the draw function?  What makes it so unique?  We know that p5js calls setup only once when the script is run and calls the draw function continuously.

What have we seen so far? We have done this.

```js
function draw()
{
    background(220);
}
```

Calling the background function repeatedly, then the user sees the grey background.  How can we tell, though? Remember when talked about writing information to the screen?  We can write to the console.log to prove that the draw is called multiple times.  Let's try it.

```js
function draw()
{
    background(220);
    console.log("hi");
}
```

Open your Developer Options and see what it says in the console?
**Note** In Chrome, you can get to the Developer Options by clicking the three vertical dots in the upper right-hand corner, then selecting **More Tools** and then **Developer tools**.
What did you see?

</div>
</div>

<div id="FinalPage" class="tabcontent">

<div class="tabhtml" markdown="1">

So, what might our final HTML page look like?

```html
<html>

    <head>
        <title>
            First p5.js page
        </title>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.1.9/p5.min.js"></script>
        <script>
            function setup()
            {
                createCanvas(300,500);
            }
            function draw()
            {
                background(220);
            }
        </script>
    </head>
    <body>

    </body>
</html>
```

Or you can separate the script into it's own page where the HTML page might look like this. Let's call the page: **main.html**. 

```html
<html>

    <head>
        <title>
            First p5.js page
        </title>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.1.9/p5.min.js"></script>
        <script src="sketch.js"></script>
    </head>
    <body>

    </body>
</html>
```

This would be the **sketch.js** file.

```js
    function setup()
    {
        createCanvas(300,500);
    }
    function draw()
    {
        background(220);
    }
    
```

Just remember the directory structure might look like this:

* 120Assignment (This might be your main folder)
    * main.html
    * sketch.js

</div>
</div>
<div id="Video" class="tabcontent">
<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/985etrz6zX4" frameborder="0" allowfullscreen></iframe></div>

</div>
</div>
<div id="ToDo" class="tabcontent">
<div class="tabhtml" markdown="1">

Make changes to the set up and draw in the editor.

<iframe src="https://editor.p5js.org/" width="100%" height="800px"></iframe>
</div>
</div>

