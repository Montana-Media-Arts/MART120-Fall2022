---
title: JavaScript Basics
module: 8
jotted: true
---

# JavaScript Basics

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
   <button class="tablinks" onclick="openTab(event, 'HTML')">Alert Example</button>
   <button class="tablinks" onclick="openTab(event, 'Document')">Document Example</button>
   <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
    
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">
<!-- video -->
<p><a href="//www.youtube.com/embed/Gf_fmLtMiI4" data-lity>JavaScript Basics Video</a></p>

<p>What is JavaScript? JavaScript is the client-side programming language that allows us to provide actual functionality to our HTML sites.</p>

<p>How is JavaScript recognized in an HTML page? We need to use <b>script</b> tags now. They look like this.</p>

<div class="tabhtml" markdown="1">

```js
 <script> </script>
```

</div>

<p>Inside the script tags are where we put our JavaScript code. These script tags can go anywhere in your HTML. Often you find them in the head tag, but they can also be at the bottom of the body tag. All major browsers read and interpret JavaScript without having to install anything extra. Nice huh?</p>

<p>What can we do right away?</p>

<p>We can <b>display</b> text in all different ways.</p>

<ol>
<li>Writing into an alert box, using window.alert().</li>
<li>Writing into the HTML output using document.write().</li>
<li>Writing into an HTML element, using innerHTML.</li>
<li>Writing into the browser console, using console.log().</li>
</ol>

</div>

<div id="HTML" class="tabcontent">

<p>Well, let's create a quick web page that looks like this.</p>

<div class="tabhtml" markdown="1">

```html
 <html>
    <title>First JavaScript Page!</title>
    <head>
        <script>
            window.alert("HI");
        </script>
    </head>
    <body>
        This HTML page has JavaScript on it. Did you see the popup?
    </body>
 </html>
```

</div>

<p>Open your webpage. Did it provide a popup? Fun huh!? And yes, annoying. Keep in mind there is a new <b>syntax</b> of which we should be aware.</p>

<p>The <b>window</b> means access to a new window object. The <b>.</b> is saying I want to access a method called <b>alert</b> that will display an alert window type. The <b>()</b> is what tells you that it is a method and that it can receive a <b>parameter</b>. In this case, the parameter is <b>Hi</b>, and it has to be surrounded by double-quotes for it to work correctly. Finally, all JavaScript lines must end with a semi-colon <b>;</b>. The semi-colon tells the computer where the line of code ends. Whew, that was a lot! Don't worry; you will see this is again and again. I just wanted to point this out.</p>

<p>What else can we do?</p>

</div>

<div id="Document" class="tabcontent">

This time change your webpage so that it looks like this.

<div class="tabhtml" markdown="1">

```html
 <html>
    <title>First JavaScript Page!</title>
    <head>
        <script>
            document.write("Hi there");
        </script>
    </head>
    <body>
        This HTML page has JavaScript on it. What do you see?
    </body>
 </html>
```

</div>

What was different this time? Do you still see the text in the body? Why?

Go onto the next section to learn about accessing HTML and making changes there.

</div>
<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="gOxPMwq" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/gOxPMwq">
  JS - Document Example</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>