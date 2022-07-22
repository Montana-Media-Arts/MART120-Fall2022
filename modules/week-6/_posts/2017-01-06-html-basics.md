---
title: HTML Basics
module: 6
jotted: false
---

# HTML Basics

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
  
  <button class="tablinks" onclick="openTab(event, 'Description')">Description</button>
  <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>  
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/CeZfpz4_abw" data-lity>HTML Basics Video</a></p>

What other tags do we need to make stuff show up?

<div class="tabhtml" markdown="1">

```html
<html>
    <head>
        <title>My First Page</title>
    </head>
    <body>
        <h1>My first website</h1>
        <p>My stuff is really important.</p>
        <br />
        How do you like them apples?
    </body>
</html>
```

</div>

</div>

<div id="Description" class="tabcontent">

<p>What are these tags?</p>

<ol>
<li><b>body</b> - this tag surrounds all the tags that are to show up in the web browser window.</li>
<li><b>h1</b> - this is a header tag. There are headers 1-6 where h1 is the largest and h6 is the smallest</li>
<li><b>p</b> - the p tag creates paragraph breaks</li>
<li><b>br</b> - the br tag creates a simple line break</li>
</ol>

</div>


<div id="ToDo" class="tabcontent">

<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="zYzbMqz" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/zYzbMqz">
  HTML Basics</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


</div>