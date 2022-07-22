---
title: Adding CSS to HTML
module: 7
jotted: true
---

# Adding CSS to HTML

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
   <button class="tablinks" onclick="openTab(event, 'Inline')">Inline Style</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p>There are three ways in which we can add CSS to an HTML page.</p>
<ol>
<li>Inline</li>
<li>Embedded</li>
<li>External</li>
</ol>
</div>

<div id="Inline" class="tabcontent">

<p><a href="//www.youtube.com/embed/ZJxsUddqZrw" data-lity>Inline CSS Video</a></p>

<p><b>Inline</b> styles are applied directly to the tag as another attribute.  Below is an example.</p>

<div class="tabhtml" markdown="1">

```html
<a href="https://www.ebay.com" style="text-decoration:none" target="_blank">Ebay</a>
```

</div>

<p>This style removes the underline from the link to eBay.  It is important to note that <b>style</b> only applies to this particular tag and no other tags on this page.  We will return to this point later.</p>

<p>What do we need to consider when we use inline styles? If we use inline styles and want that style on another page, we will need to duplicate the style on that page.  Not bad unless we have many pages with multiple tags that need to be changed.</p>

</div>
<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="eYRaBOQ" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/eYRaBOQ">
  Inline Style</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>