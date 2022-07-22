---
title: If statements
module: 8
jotted: true
---

# If statements

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Step1')">Step 1</button>
    <button class="tablinks" onclick="openTab(event, 'Step2')">Step 2</button>
    <button class="tablinks" onclick="openTab(event, 'Step3')">Step 3</button>
    <button class="tablinks" onclick="openTab(event, 'Step4')">Step 4</button>
    <button class="tablinks" onclick="openTab(event, 'Step5')">Step 5</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

<p><a href="//www.youtube.com/embed/Lxocm28nvwo" data-lity>If statements Video</a></p>

Let's start with a form that is similar to what we had before. However, this time, we have two functions. **gasp**.

</div>
</div>

<div id="Step1" class="tabcontent">

<div class="tabhtml" markdown="1">


It looks like this.

```html
<html>
    <title>If statements</title>
    <head>
        <script>
            function printQuestion()
            {
                document.getElementById("theQuestion").innerHTML = "What is 3+5?"; 
            }
            function checkAnswer()
            {
                var answer = document.getElementById("txtAnswer").value;
                document.getElementById("finalResult").innerHTML = "Your answer is " + answer;
            }
        </script>
    </head>
    <body onload="printQuestion();">
        <div id="theQuestion"></div>
        <table>
            <tr>
                <td>Your answer</td>
                <td><input type="text" id="txtAnswer"></td>
            </tr>
            <tr>
                <td colspan="2"><button id="btnSubmit" onClick="checkAnswer();">Submit</button></td>
            </tr>
        </table>
        <div id="finalResult"></div>
    </body>
 </html>
```

Okay, so first, the onLoad calls the **printQuestion** function. Then the button click calls **checkAnswer** function and the user's answer displays. Did it work for you? Good!

So, how do we know if it is correct? That is where **if** statements come in. Again, you have seen these before in other languages, but maybe not quite like this. Hopefully, you can visualize them, though. 

</div>
</div>

<div id="Step2" class="tabcontent">

<div class="tabhtml" markdown="1">


Let's change the code a bit, so it looks like this now.

```html
<html>
    <title>If statements</title>
    <head>
        <script>
        function printQuestion()
        {
            document.getElementById("theQuestion").innerHTML = "What is 3+5?";
        
        }
        function checkAnswer()
        {
            var answer = document.getElementById("txtAnswer").value;
            if(answer == 8)
            {
                document.getElementById("finalResult").innerHTML = "Good job!";
            }
            else
            {
                document.getElementById("finalResult").innerHTML = "Not quite!";
            }
        
        }
        </script>
    </head>
    <body onload="printQuestion();">
        <div id="theQuestion"></div>
        <table>
            <tr>
                <td>Your answer</td>
                <td><input type="text" id="txtAnswer"></td>
            </tr>
            <tr>
                <td colspan="2"><button id="btnSubmit" onClick="checkAnswer();">Submit</button></td>
            </tr>
        </table>
        <div id="finalResult"></div>
    </body>
 </html>
```

Run this and try entering **8**. Did you get the **Good job!** message? What about if you enter something that is not 8?

You have written an if statement in JavaScript! Good job!

</div>
</div>

<div id="Step3" class="tabcontent">

<div class="tabhtml" markdown="1">

Let's expand on this a bit now. At the moment, it's bland because it has one question. How do we make it more dynamic?

Let's create random numbers.

How do we do that?

```js
 Math.floor(Math.random() * 10);
```

Before you start breathing heavily, consider this. **Math.floor** means if there are any numbers after the decimal point (e.g., 3.453 rounds down to 3, and 3.646 also results in 3.) 

The **Math.random()** is just a function that returns a number between 0 inclusive and one exclusive. That means include zero in the results, and all decimal numbers up to 1, but not 1.  

Another thing to notice is that it's being multiplied by 10. In programming, the `*` is the multiplication sign. 

So, the number returned by Math.random (something between 0 and .9999999999) is first multiplied by ten before calling Math.floor. After all that, you will get a number between 0 and 9. If you change the 10, you will get an amount between 0 and whatever that number entered minus 1. Make sense?

</div>
</div>

<div id="Step4" class="tabcontent">

<div class="tabhtml" markdown="1">

So, how do we apply this?

```html
<html>
    <title>If statements</title>
    <head>
        <script>
        var actualAnswer;
        function printQuestion()
        {
            var number1 = Math.floor(Math.random() * 10);
            var number2 = Math.floor(Math.random() * 10);
            actualAnswer = number1 + number2;
            document.getElementById("theQuestion").innerHTML = "What is " + number1 + "+" + number2 + "?";
        
        }
        function checkAnswer()
        {
            var answer = document.getElementById("txtAnswer").value;
            if(answer == 8)
            {
                document.getElementById("finalResult").innerHTML = "Good job!";
            }
            else
            {
                document.getElementById("finalResult").innerHTML = "Not quite!";
            }      
        }
        </script>
    </head>
    <body onload="printQuestion();">
        <div id="theQuestion"></div>
            <table>
                <tr>
                    <td>Your answer</td>
                    <td><input type="text" id="txtAnswer"></td>
                </tr>
                <tr>
                    <td colspan="2"><button id="btnSubmit" onClick="checkAnswer();">Submit</button></td>
                </tr>
            </table>
        <div id="finalResult"></div>
    </body>
 </html>
```

I did two things right away.

1. I created three variables above the printQuestion function. I created **number1**, **number2**, and **actualAnswer** variables (look for the **var**). I put the number1 and number2 variables in the printQuestion method because I don't need to use them in any other function. However, we use actualAnswer in both the printQuestion and the checkAnswer functions. If we declared actualAnswer in the printQuestion function, the checkAnswer function wouldn't be able to use it.

Put this into your web page. Do you see a different question when you run it? What if you answer it? Did you get the **Good job!** with the correct answer? Why or why not?

</div>
</div>

<div id="Step5" class="tabcontent">

<div class="tabhtml" markdown="1">
What do we need to change?

The code should look like this.

```html
<html>
    <title>If statements</title>
    <head>
    <script>
        var actualAnswer;
        function printQuestion()
        {
            var number1 = Math.floor(Math.random() * 10);
            var number2 = Math.floor(Math.random() * 10);
            actualAnswer = number1 + number2;
            document.getElementById("theQuestion").innerHTML = "What is " + number1 + "+" + number2 + "?";
            
        }
        function checkAnswer()
        {
            var answer = document.getElementById("txtAnswer").value;
            if(answer == actualAnswer)
            {
                document.getElementById("finalResult").innerHTML = "Good job!";
            }
            else
            {
                document.getElementById("finalResult").innerHTML = "Not quite!";
            }
        
        }
    </script>
    </head>
    <body onload="printQuestion();">
        <div id="theQuestion"></div>
             <table>
                <tr>
                    <td>Your answer</td>
                    <td><input type="text" id="txtAnswer"></td>
                </tr>
                <tr>
                    <td colspan="2"><button id="btnSubmit" onClick="checkAnswer();">Submit</button></td>
                </tr>
            </table>
        <div id="finalResult"></div>
    </body>
 </html>
```

Next, let's look at how we can do this more than once by using a for loop.
</div>
</div>
<div id="ToDo" class="tabcontent">
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="qBXbNPY" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/qBXbNPY">
  JS - if statements</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>