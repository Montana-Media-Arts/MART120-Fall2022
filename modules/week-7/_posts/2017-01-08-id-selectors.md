---
title: ID Selectors
module: 7
jotted: true
---

# ID Selectors

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'HTML')">HTML Example</button>
    <button class="tablinks" onclick="openTab(event, 'CSS')">ID Selectors Example</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/Zfb_V1-lI1E" data-lity>ID Selectors Video</a></p>

<p>Another way in which we can select a tag is by their ID if they have an id attribute defined. </p>

</div>

<div id="HTML" class="tabcontent">

<p>The HTML page might look like this.</p>

<div class="tabhtml" markdown="1">

```html
    <html>
        <head>
            <title>id Example</title>
            <link rel="stylesheet" type="text/css" href="mainstyle.css">
        </head>
        <body>
            <span id="specificColor">New Color</span>
            <br>
            <span>Same Color</span>
            <br>
            <a href="https://www.amazon.com" id="specificLink" target="_blank">Amazon</a>
        </body>
    </html>
```

</div>

</div>

<div id="CSS" class="tabcontent">

<p>And the CSS might look like this.</p>

<div class="tabhtml" markdown="1">

```css
    #specificColor{
        color:blue;
        font-family:verdana;
        font-size:24px;
    }

    #specificLink{
        color:red;
        font-family:arial;
        font-size:28px;
    }
```

</div>

<p>This time, the color and the size of the text specific to the ID because of the <b>#</b>.</p>

</div>
<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="mdwYOVO" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/mdwYOVO">
  id Selector</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>