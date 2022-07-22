---
title: Class Selectors
module: 7
jotted: true
---

# Class Selectors

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'HTML')">HTML Page Example</button>
    <button class="tablinks" onclick="openTab(event, 'CSS')">Class Selectors Example</button>
     <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/kkFsRWlswX0" data-lity>Class Selectors Video</a></p>

<p>In the previous section, we added styles by using inline styles, embedded styles, and external style sheets.</p>

<p>In our styles, we were general to all span tags.  However, what if we wanted to find a specific tag or apply a style to several different tags?  That is where we use classes and ids in our stylesheets.  We will use stylesheets from now on.</p>

</div>

<div id="HTML" class="tabcontent">

Here's an example of an HTML page.

<div class="tabhtml" markdown="1">

```html
    <html>
        <head>
            <title>Class Example</title>
            <link rel="stylesheet" type="text/css" href="mainstyle.css">
        </head>
        <body>
            <span class="blueColor">New Color</span>
            <br>
            <span>Same Color</span>
            <br>
            <a href="https://www.amazon.com" class="blueColor" target="_new">Amazon</a>
        </body>
    </html>
```

</div>

</div>

<div id="CSS" class="tabcontent">

<div class="tabhtml" markdown="1">

```css
    .blueColor{
        color:blue;
        font-family:arial;
        font-size:24px;
    }
```

</div>

<p>Notice in this example, the CSS has the name <b>.blueColor</b>.  The blueColor class identifier applies the blue color, changes the font type, and the size of the <b>span</b> tag and an <b>a</b> (anchor) tag.  They both turned blue while the other span tag without the class name did not.</p>

<p>We can get even more specific by doing something like this.</p>

<div class="tabhtml" markdown="1">

```css
    span.blueColor{
        color:blue;
        font-family:arial;
        font-size:24px;
    }
```

</div>

<p>Now, only span tags with the class <b>blueColor</b> will change.  No other tags will work.</p>

</div>
<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="GREaNpr" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/GREaNpr">
  Class Selector</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>