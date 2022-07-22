---
title: Accessing HTML Tags
module: 8
jotted: true
---

# Accessing HTML Tags

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
   <button class="tablinks" onclick="openTab(event, 'ById')">getElementById Example</button>
    <button class="tablinks" onclick="openTab(event, 'Document')">document.write Example</button>
    <button class="tablinks" onclick="openTab(event, 'Debug')">debug Example</button>
     <button class="tablinks" onclick="openTab(event, 'Console')">console.log Example</button>
     <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
    
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/1aQplfKL2eI" data-lity>Accessing HTML Tags Video</a></p>

<p>One of the most useful things that JavaScript can do is access HTML tags and change their content. Look at the example in the next tab.</p>

</div>

<div id="ById" class="tabcontent">

<div class="tabhtml" markdown="1">

```js
 document.getElementById("myTag").innerHTML = "New Text";
```

</div>

<p>If you were to have an HTML page like the following, the JavaScript above would change the tag with the id "myTag".</p>

<div class="tabhtml" markdown="1">

```html
 <html>
    <body>
        <span id="myTag">This is my favorite text</span>
    </body>
 </html>
```

</div>

</div>


<div id="Document" class="tabcontent">

<p>Another way to access HTML is by using the document.write function.  It looks something like this.</p>

<div class="tabhtml" markdown="1">

```js
 document.write("I am being written to the HTML page");
```

</div>

<p>But what if there is an error? For example, what if we misspell something or put the script tag in the wrong place?</p>

<p>Initially, we put the script tag in the head tag.</p>

</div>


<div id="Debug" class="tabcontent">

<p>However, when the browser renders the HTML, it is read from top to bottom. So, if the JavaScript is at the top and you try to access an HTML element in the body, it won't be found.  Or, if you misspell a function name, an error will occur as well.  However, web pages won't show you the error. Browsers do their best to show what they can.</p>

<p>For example, if you were doing the following.</p>

<div class="tabhtml" markdown="1">

```html
 <html>
    <head>
        <script>
            document.getElementById("myTag").innerHTML = "New Text";
        </script>
    </head>
    <body>
        <span id="myTag">This is my favorite text</span>
    </body>


 </html>
```

</div>

<p>The previous code will cause an error. We can fix this error by doing the following.</p>

<div class="tabhtml" markdown="1">

```html
 <html>
    <body>
        <span id="myTag">This is my favorite text</span>
    </body>

    <script>
        document.getElementById("myTag").innerHTML = "New Text";
    </script>
 </html>
```

</div>


However, if we mistype something like this:

<div class="tabhtml" markdown="1">

```html
 <html>
    <body>
        <span id="myTag">This is my favorite text</span>
    </body>

    <script>
        dcument.getElementById("myTag").innerHTML = "New Text";
    </script>
 </html>
```

</div>

<p>We will also get an error.</p>

<p>How do we fix it?</p>

<p>It's in the browser settings. To access those in Chrome, follow these steps.</p>

<ol>
<li>Click on the three vertical dots in the upper right-hand corner of the web browser.</li>
<li>Navigate to <b>More Tools</b>-><b>Developer Tools</b></li>
<li>Click on the console tab. The area shows you the error and where it is in your code. Nice!</li>
</ol>

</div>

<div id="Console" class="tabcontent">

<p>We can also use another command to write to the console. It's called console.log.</p>

<p>Try this now.</p>

<div class="tabhtml" markdown="1">

```html
 <html>
    <body>
        <span id="myTag">This is my favorite text</span>
    </body>

    <script>
        console.log("I am in the console!");
    </script>
 </html>
```

</div>

<p>Open your web page. It won't show anything on the page. However, if you go to the console in the Developer Tools again, you will see the console.log message. Console.log is an excellent way to find out what is happening in your JavaScript code.</p>

<p>Next, let's talk about variables in JavaScript.</p>
</div>

<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="QWMyEdb" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/QWMyEdb">
  JS - getElementById</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>