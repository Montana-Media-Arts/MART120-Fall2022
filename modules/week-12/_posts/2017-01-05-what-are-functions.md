---
title: What are Functions
module: 13
jotted: false
---

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Example')">Example</button>
      <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
    
</div>

<div id="Overview" class="tabcontent" style="display:block">
<div class="tabhtml" markdown="1">

# Definition

Functions combine multiple lines of code to perform an actions.  What happens is that functions take several lines of code and combine them into a single line.

Here is another to explain them.

Every programming language lets you create blocks of code that, when called, perform tasks. Imagine a dog that does the same trick only when asked. Except you do not need dog treats to make your code perform. In programming, these code blocks are called functions.

All programming functions have input and output. The function contains instructions used to create the output from its input. It’s like a cow that eats grass (the input) which its body turns into milk which a dairy farmer then milks (the output).

For example, programming functions might take as input any integer or number. The function might create output by multiplying the input times two. Therefore, the output of the function would be double its input.

Or imagine the short Hello message you sometimes see in online software applications at the top right corner of any page. The function would take as input your name (or user number) from the application and drop your name (or look up your name with your user number) into the phrase “Hello [your name]!” If your name is Jane, the output of this function would be “Hello Jane!”

It is possible to build entire software applications with only functions. Programming languages which primarily use functions are called functional programming languages. Haskell and a few other languages are primarily functional languages. You build software by building blocks of code that perform specific tasks.

<em><a href="https://www.kidscodecs.com/programming-functions/" target="_blank">Source</a></em>
</div>
</div>

<div id="Example" class="tabcontent" >

<div class="tabhtml" markdown="1">

## Example

What does that mean?  Well, let's think about one of the main functions we already use.

```js
    
    function draw()
    {

    }
```
`draw` is a function that is called continously when a sketch runs.  

## Parts of a functions

```js
    function draw()
    {

    }
```

Let's breakdown the `draw` function.  

1. A function in p5.js always starts with the keyword **function**.  
2. It is followed by the **name** of the function, in this case, **draw**.
3. The function name is always followed by **()** parentheses.  **Note** The parentheses can contain parameters, which we will discuss in the next section.
4. Finally, the **body** of the function is surrounded by **{}** curly braces.

The draw function is built-in to p5.js.  All programming languages have built-in functions.  However, programmers can define functions too.

</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/-JoLD2QXWeU" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
<div id="ToDo" class="tabcontent" >
<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="LYjgovb" data-editable="true" data-user="retrog4m3r" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/retrog4m3r/pen/LYjgovb">
  Intro to Functions - p5.js</a> by Michael Cassens (<a href="https://codepen.io/retrog4m3r">@retrog4m3r</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>