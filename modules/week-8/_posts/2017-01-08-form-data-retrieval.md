---
title: Form Data Retrieval
module: 8
jotted: true
---

# Form Data Retrieval
<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
   <button class="tablinks" onclick="openTab(event, 'Step1')">Step 1</button>
   <button class="tablinks" onclick="openTab(event, 'Step2')">Step 2</button>
    <button class="tablinks" onclick="openTab(event, 'Step3')">Step 3</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
    
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/nUNz4RvgZdo" data-lity>Form Data Retrieval Video</a></p>

Keep in mind that although it's handy to print information to the page, it is beneficial to get information from a form. I imagine most of you have filled out web forms before. They are super fun, I know. However, most web forms use JavaScript in one way or another. So, we are going that.

</div>

<div id="Step1" class="tabcontent">

<div class="tabhtml" markdown="1">

Let's create a form like this.

```html
<html>
    <title>Forms</title>
    <head>
        
    </head>
    <body>
        <table>
            <tr>
                <td>Name</td>
                <td><input type="text" id="txtName"></td>
            </tr>
            <tr>
                <td>Phone Number</td>
                <td><input type="text" id="txtPhone"></td>
            </tr>
            <tr>
                <td colspan="2"><button id="btnSubmit" onClick="getData();">Submit</button></td>
            </tr>
        </table>
    </body>
 </html>
```

If you put this into your web page, you will see a basic form. It won't be fancy (there is no styling, as you know). So, how do we make it function?

</div>
</div>

<div id="Step2" class="tabcontent">

<div class="tabhtml" markdown="1">

Let's change the form now to look like this.

```html
<html>
    <title>Forms</title>
    <head>
        <script>
            function getData()
            {
                var name = document.getElementById("txtName").value;
                var phone = document.getElementById("txtPhone").value;

                window.alert("name: " + name + " phone: " + phone);
            }
        </script>
    </head>
    <body>
        <table>
            <tr>
                <td>Name</td>
                <td><input type="text" id="txtName"></td>
            </tr>
            <tr>
                <td>Phone Number</td>
                <td><input type="text" id="txtPhone"></td>
            </tr>
            <tr>
                <td colspan="2"><button id="btnSubmit" onClick="getData();">Submit</button></td>
            </tr>
        </table>
    </body>
 </html>
```

There are a couple of things to notice here.

1. Within the button tag, there is an **onClick** event called now. It calls the function **getData**. We know it's a function because of the **()** after the name.
2. If we go to the script tags within the head tag, you will find the getData function. It retrieves the data from the text boxes by calling the **value** property.
3. Variables store the values, and then we use the window.alert to determine if we are getting the actual values.

Why did I do that? Percolate on that for a second.

I did it because then we know we are getting the correct data before we write more code. We don't want to keep going only to find out that none of it is working. If we have a whole lot of code to wade through, it can get harrowing. If you don't like window.alert, you can always use console.log. It is just as useful.

</div>
</div>

<div id="Step3" class="tabcontent">

<div class="tabhtml" markdown="1">

So, now that it is working, let's print out the values on the page. It looks like this.

```html
<html>
    <title>Forms</title>
    <head>
        <script>
            function getData()
            {
                var name = document.getElementById("txtName").value;
                var phone = document.getElementById("txtPhone").value;

                document.getElementById("finalResult").innerHTML = "name: " + name + " phone: " + phone;
            }
        </script>
    </head>
    <body>
        <table>
            <tr>
                <td>Name</td>
                <td><input type="text" id="txtName"></td>
            </tr>
            <tr>
                <td>Phone Number</td>
                <td><input type="text" id="txtPhone"></td>
            </tr>
            <tr>
                <td colspan="2"><button id="btnSubmit" onClick="getData();">Submit</button></td>
            </tr>
        </table>
        <div id="finalResult"></div>
    </body>
 </html>
```

All I did was add a **div** tag and then accessed its Id in JavaScript and put the name and phone number in that tag. 

Where do we go from here? Let's create a small addition game to learn about **if** statements in JavaScript.
</div>
</div>

<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="XWaXKag" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/XWaXKag">
  JS Form Retrieval</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

</div>