---
title: More form elements
module: 6
jotted: true
---

# More form elements

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Dropdown')">Dropdown List</button>
  <button class="tablinks" onclick="openTab(event, 'Radio')">Radio Buttons</button>
  <button class="tablinks" onclick="openTab(event, 'Checkbox')">Checkboxes</button>
  <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
    
</div>

<!-- Tab content -->
<div id="Dropdown" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/rJJ-rnX3SPM" data-lity>Drop Downlist Video</a></p>
<!-- dropdowns -->

<p>One of the most common form elements is the drop-down list.  It looks something like this.</p>

<div class="tabhtml" markdown="1">

```html
<select>
  <option value="apples">Apples</option>
  <option value="oranges">Oranges</option>
  <option value="grapes">Grapes</option>
  <option value="pineapple">Pineapple</option>
</select>
```

</div>

These allow us to restrict what the user can choose and helps us make sure we get data precisely the way we want it. If we use a text box for everything, then our users could type anything they wanted.  For example, they might say <b>Apple</b>, or <b>aPpple</b>, or <b>APPLE</b>, and that would be bad.
</div>

<div id="Radio" class="tabcontent">

<!-- video -->

<p><a href="//www.youtube.com/embed/Mzx_lShObmc" data-lity>Radio Button Video</a></p>

<!-- radio -->
<b>What other items can you find in forms?  I spoke of radio buttons and checkboxes in an earlier section.  How would you implement a radio button list?</b>

<div class="tabhtml" markdown="1">

```html
<input type="radio" name="color" value="blue">Blue<br>
<input type="radio" name="color" value="red">Red<br>
<input type="radio" name="color" value="green">Green<br>
<input type="radio" name="color" value="purple">Purple
```

</div>

</div>

<div id="Checkbox" class="tabcontent">

<!-- video -->
<p><a href="//www.youtube.com/embed//28ccGRjnV_Q" data-lity>Checkbox Video</a></p>

<!-- checkboxes -->
<p>Finally, let's look at checkboxes and the role they play in forms.  They allow us to select multiple items in a list.  We see these most often when a form asks us what our interests are.  It may look something like this.</p>

<div class="tabhtml" markdown="1">

```html
<h2>What kind of bikes do you like?</h2>
<input type="checkbox" name="mountain" value="mountain">Mountain<br>
<input type="checkbox" name="road" value="road">Road<br>
<input type="checkbox" name="cross" value="cross" checked>Cross<br>
<input type="checkbox" name="fattire" value="fattire" checked>Fat Tire<br>
<input type="checkbox" name="gravel" value="gravel" checked>Gravel<br>
```

</div>

</div>

<div id="ToDo" class="tabcontent">

<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="vYZPQzw" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/vYZPQzw">
  More Form Elements</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>