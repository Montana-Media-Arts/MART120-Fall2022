---
title: HTML Forms
module: 6
jotted: true
---

# HTML Forms

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
  <button class="tablinks" onclick="openTab(event, 'Example')">Example</button>
  <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
    
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/LJ0Ldc_2B8M" data-lity>HTML Forms Video</a></p>

<p>What are HTML forms?  If you have ever purchased something online or filled out an application online or signed up for an email, your social media account, or more, you have filled out a form.  Forms are just a way for us to gather data from the end-user.  Keep in mind there are some principles to which we should adhere.</p>

<p>First, we want to adhere to standards. Use the component for their intended use.  Use checkboxes for multiple selections and radio buttons for various choices, but only one correct one.</p>

<p>Aso, use dropdown lists, use those to control the input gathered.  We are going to first focus on creating forms and what tags are required. Then, we will add a look and feel to them and add a little functionality to them.</p>

</div>

<div id="Example" class="tabcontent">

<p>Here is an example of a simple form.</p>

<div class="tabhtml" markdown="1">

```html
<html>
    <head>
        <title>My first page</title>
    </head>
    <body>
        
        <form action="nextPage.html" type="Post">
            First Name: <input type="text" id="fName"><br>
            Last Name: <input type="text" id="lName"><br>
            <button id="mySubmit" type="submit">Submit</button>
        </form>
    </body>
</html>

```

</div>

</div>
<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="rNwRQrY" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/rNwRQrY">
  HTML Forms</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>