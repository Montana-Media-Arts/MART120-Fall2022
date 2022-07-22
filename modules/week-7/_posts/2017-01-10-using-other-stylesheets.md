---
title: Using other Styles
module: 7
jotted: true
---

# Using other StyleSheets

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'CDN')">CDN</button>
    <button class="tablinks" onclick="openTab(event, 'Local')">Local Copy</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/qu0rslp1jho" data-lity> Using Other Stylesheets Video</a></p>

<p>There are some popular stylesheets out there. One of the most popular is Bootstrap.  To use it, we have a couple of options. We have two options.</p>

<ol>
<li>Use a CDN</li>
<li>Download a local copy and reference the local copy.</li>
</ol>
</div>

<div id="CDN" class="tabcontent">

<p><b>CDN Example</b></p>

<div class="tabhtml" markdown="1">

```html
<html>
    <head>
        <title>Other Library Example</title>
          <meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
    </head>
    <body>
        <button type="button" class="btn">Basic</button>
        <button type="button" class="btn btn-default">Default</button>
        <button type="button" class="btn btn-primary">Primary</button>
        <button type="button" class="btn btn-success">Success</button>
        <button type="button" class="btn btn-info">Info</button>
        <button type="button" class="btn btn-warning">Warning</button>
        <button type="button" class="btn btn-danger">Danger</button>
        <button type="button" class="btn btn-link">Link</button>
    </body>
</html>
```

</div>

<p></p>
<p>Take a look at the <b>href</b> attribute in the <b>link</b> tag at the top inside the <b>head</b> tag. It points to what is called a CDN.  CDN stands for <b>Content Delivery Network</b> There are some benefits to using these.  Your CSS is always up to date whenever the author updates it.  However, it only works if you are online to apply this style. So, if you need an offline application, you may want to use a local copy.</p>

</div>

<div id="Local" class="tabcontent">

<p>In the case of Bootstrap, you first go to:</p>

<ol>
<li>Go to <a href="https://getbootstrap.com/" target="_blank">Get Bootstrap</a></li>
<li>Then, click on <b>Download</b>.</li>
<li>Under <b>Compiled CSS and JS</b>, click <b>Download</b>.</li>
<li>Download the zip file.</li>
<li>Unzip and save the folder in a directory near your web page file.</li>
<li>Download JQuery from: <a href="https://jquery.com/" target="_blank">Get jQuery</a></li>
<li>Then, click on <b>Download jQuery</b>.</li>
<li>Right-click <b>Download the compressed, production jQuery 3.x.x</b> and save the file in your <b>js</b> folder with Bootstrap.</li>
<li>Reference bootstrap like this (if your folder structure is set up like the following).</li>
</ol>

<div class="tabhtml" markdown="1">

```html
<html>
    <head>
        <title>Other Library Example</title>
          <meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="./styles/bootstrap-4.3.1/css/bootstrap.min.css">
<script src="./styles/bootstrap-4.3.1/js/jquery-3.4.1.min.js"></script>
<script src="./styles/bootstrap-4.3.1/js/bootstrap.min.js"></script>
    </head>
    <body>
        <button type="button" class="btn">Basic</button>
        <button type="button" class="btn btn-default">Default</button>
        <button type="button" class="btn btn-primary">Primary</button>
        <button type="button" class="btn btn-success">Success</button>
        <button type="button" class="btn btn-info">Info</button>
        <button type="button" class="btn btn-warning">Warning</button>
        <button type="button" class="btn btn-danger">Danger</button>
        <button type="button" class="btn btn-link">Link</button>
    </body>
</html>
```

</div>

<p>Did you see the same thing as before?  Unfortunately, it's not as simple as using a CDN. However, if you need an offline solution, this will work.  Downloading and saving libraries work for other styles (and JavaScript) that you may want to use in the future too.</p>

</div>
<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="mdwYOPO" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/mdwYOPO">
  Bootstrap Example</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>