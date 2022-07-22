---
title: External Style Sheets
module: 7
jotted: true
---

# Adding CSS to HTML

## External Style Sheets

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Stylesheet')">External Stylesheet</button>
    <button class="tablinks" onclick="openTab(event, 'Page')">HTML Page</button>
    <button class="tablinks" onclick="openTab(event, 'Order')">Ordering of Styles</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/SgCWkF4--t0" data-lity>External CSS Video</a></p>

<p>The last way in which we can apply a style is through an <b>external</b> style sheet.</p>

</div>

<div id="Stylesheet" class="tabcontent">

<p>How does the stylesheet look?</p>

<div class="tabhtml" markdown="1">

```css
span{
    color:white;
    background-color:red;
}
```

</div>

<p>Note that when you save this on a separate page, it must be called <b>mainstyle.css</b>  It always ends with a <b>.css</b> extension.</p>

</div>

<div id="Page" class="tabcontent">

<p>Now, we can assign it to a page like this.</p>

<div class="tabhtml" markdown="1">

```html
    <html>
        <head>
            <title>External Style Sheet</title>
            <link rel="stylesheet" type="text/css" href="mainstyle.css">
        </head>
    </html>
```

</div>

<p></p>

<p>There are a couple of things to note.  The <b>rel</b> is the relationship attribute, and the <b>type</b> specifies the type of file.  Finally, the <b>href</b>, which should look familiar, is the file location. Remember, if it defined like it is above, it has to be in the same folder.  Otherwise, you need to add the correct path.</p>

<p>We use style sheets so that we can apply a style sheet to many pages.  If we want to make a change, we can change it in one file and use it everywhere.</p>

</div>

<div id="Order" class="tabcontent">

<p>So, when you have all three types of styles on your page, which style is applied?  It always goes in this order.</p>

<ol>
<li>Inline styles first</li>
<li>Embedded</li>
<li>External</li>
<li>Browser</li>
</ol>

<p>Yes, that's right; the browser has a style sheet.  If you are interested, take a look around, and you can find and change your browser's style sheet. Fun right?</p>

</div>

<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="RwgmoPR" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/RwgmoPR">
  External Style</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>