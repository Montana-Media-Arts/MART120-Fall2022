---
title: Functions
module: 8
jotted: false
---

# Functions

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
   <button class="tablinks" onclick="openTab(event, 'Functions')">Functions Example</button>
   <button class="tablinks" onclick="openTab(event, 'HTML')">HTML Example</button>
    <button class="tablinks" onclick="openTab(event, 'Parameters')">Parameters Example</button>
     <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
    
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/BN25BnXgYNo" data-lity>Functions Video</a></p>

<p>If you recall when we changed the text in the span tag, we had to put the JavaScript script at the bottom so that it wouldn't give us an error.</p>

<p>What if we wanted to make it so that the JavaScript code didn't run automatically. Insert <b>functions</b>. You have seen them already. You used them with <b>alert</b>, <b>log</b>, <b>write</b>, <b>getElementById</b>. Now we are going to create one ourselves. </p>

</div>

<div id="Functions" class="tabcontent">

<p>Functions look like this.</p>

<div class="tabhtml" markdown="1">

```js
 function myFunction()
 {
    window.alert("Hi there!");
 }
```

</div>

<p>We just created a function called <b>myFunction</b>, and it contains one line of code, which just so happens to be another window.alert. However, it will not run unless we call myFunction somewhere.</p>

<p>You might notice that there are <b>{}</b> before and after the window.alert. These indicate where the function body begins and ends. Without them, the function doesn't work.</p>

</div>

<div id="HTML" class="tabcontent">

<div class="tabhtml" markdown="1">

What does this look like on a full page?

```html
<html>
    <title>Functions</title>
    <head>
        <script>
            function displayFavoriteColor()
            {
                var favoriteColor = "blue";
                document.getElementById("myTag").innerHTML = "Favorite Color " + favoriteColor;
            }       
        </script>
    </head>
    <body>
        <span id="myTag">This is my favorite text</span>
    </body>
 </html>
```

Not calling the function, results in the original text shown. How do we call this function? Below is one way.

```html
<html>
    <title>Functions</title>
    <head>
        <script>
            function displayFavoriteColor()
            {
                var favoriteColor = "blue";
                document.getElementById("myTag").innerHTML = "Favorite Color " + favoriteColor;
            }       
        </script>
    </head>
    <body onload="displayFavoriteColor();">
        <span id="myTag">This is my favorite text</span>
    </body>
 </html>
```

Placing the function name in the **onload** event of the body is one way to call the function. This event is just a unique attribute of the body and allows us to call JavaScript functions. Neat huh?

Now the text should be changed right when you open the page.

</div>
</div>

<div id="Parameters" class="tabcontent">

<div class="tabhtml" markdown="1">

What about parameters?

An example of calling parameters looks like this.
```html

<html>
    <title>Functions</title>
    <head>
    <script>
        function displayFavoriteColor(color)
        {
            var favoriteColor = color;
            document.getElementById("myTag").innerHTML = "My favorite color is " + favoriteColor;
        }
    </script>
    </head>
    <body onload="displayFavoriteColor('blue');">
        <span id="myTag">This is my favorite text</span>
    </body>
</html>
 ```
We declare the variable in the displayFavoriteColor function.  It is called **color**.  Then, we assign that variable to the favoriteColor variable in the function.  Then, in the onload event, we pass in a value.  In this case, we pass in a value of **blue** inside of single quotes.  We do this because the onload puts the function call inside of double-quotes.

What about getting information from a form or something like that? Move on, and you will find out!

</div>
</div>
<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="eYEJzRv" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/eYEJzRv">
  JS - Functions Parameters</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>

