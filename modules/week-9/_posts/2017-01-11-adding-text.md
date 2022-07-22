---
title: Adding Text
module: 9
jotted: false
---

# Adding Text

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Basic')">Basic Text</button>
    <button class="tablinks" onclick="openTab(event, 'Size')">Text Size</button>
     <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
     <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Basic" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

Adding text on your page is not too difficult.  We have to use the text function.  It looks like this.

```js
function setup() {
  createCanvas(400,400);
}

function draw() {
    background(220);
    text('Hello there!', 10, 30);
}
```

This prints the words **Hello there!** to the screen at location x-location 10 and y-location 30.

</div>
</div>
<div id="Size" class="tabcontent">

<div class="tabhtml" markdown="1">


Notice how it's not too big, though?  We can change the size of the font but using the textSize function.  It looks like this.

```js
function setup() {
  createCanvas(400,400);
}

function draw() {
    background(220);
    textSize(32);
    text('Hello there!', 10, 30);
}
```

You see that the text is much larger and readable, well, at least for me since I cannot see that well. Okay, now you are ready for your homework!
</div>
</div>

<div id="Video" class="tabcontent">
<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/eUegipUHNlo" frameborder="0" allowfullscreen></iframe></div>

</div>
</div>

<div id="ToDo" class="tabcontent">
<div class="tabhtml" markdown="1">

Try adding some text to the draw function.

<iframe src="https://editor.p5js.org/" width="100%" height="800px"></iframe>
</div>
</div>