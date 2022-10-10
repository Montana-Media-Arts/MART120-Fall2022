---
title: Setup the Scene
module: 12
jotted: false
---

# Setup the Scene

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Setup')">Setup</button>
    <button class="tablinks" onclick="openTab(event, 'Movement')">Movement</button>
     <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>

</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

I find in programming that often is it is useful to have some context indicating why I am creating something.  That is why  I had you create a self-portrait. Now, we are going to create some interactive art using events.
</div>
</div>

<div id="Setup" class="tabcontent">

<div class="tabhtml" markdown="1">

First, let's set up our scene.

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
    }
```

Here we just created a simple black background and added a greenish circle to it.
</div>
</div>

<div id="Movement" class="tabcontent">

<div class="tabhtml" markdown="1">

We know how to make it move.

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
        x+=10;
    }
```

That moves our circle to the right because we are adding to x.  Remember that x,y, and diameter are variables.  We are just changing (or can change) the values stored in those variables, which makes them useful.  Yes?  Good!

Hopefully, you also found out that if you change x and y and diameter at the same time, some exciting things happen.  The concepts we learned last week will be the starting point for this week.

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
        x+=10;
        y+=3;
        diameter+=8;
    }
```

Fun! Where do we go from here? Let's talk about the conditions.  What are those? If, if/else, and if/else if statements.  We have seen the first two, but maybe not the third one. We will look at those.

</div>
</div>

<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/nTtrvVHO3U0" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>

<div id="ToDo" class="tabcontent">
<div class="tabhtml" markdown="1">

<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="JjymQGE" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/JjymQGE">
  p5.js Movement</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>
</div>