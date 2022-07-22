---
title: Constructor Method
module: 14
jotted: false
---

# Class Constructor Methods

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
  <button class="tablinks" onclick="openTab(event, 'Example')">Example</button>
  <button class="tablinks" onclick="openTab(event, 'Video')">Video</button>
</div>

<div id="Overview" class="tabcontent" style="display:block"  >
<div class="tabhtml" markdown="1">

In p5.js classes there is a `constructor` function. This should be the first function defined in the class.

The constructor function **is always** called when creating a new object from a class. Therefore you **must** have a constructor function. You can think about it as 'constructing' or building a new object. The _constructor_ function is how a new object gets built."

</div>
</div>

<div id="Example" class="tabcontent">
<div class="tabhtml" markdown="1">

In the previous section, the class looked like this.

```js
class Dog {
  constructor(name, breed, weight, eyeColor, hairColor ) {
    this.name = name;
    this.breed = breed;
    this.weight = weight;
    this.eyeColor = eyeColor;
    this.hairColor = hairColor;
  }

  eat()
  {
    text(this.name + "is eating...", 100, 100);
  }

  sleep()
  {
    text(this.name + " is sleeping...", 200, 200);
  }
}
```

The constructor is defined at the top like this.

```js
constructor(name, breed, weight, eyeColor, hairColor ) {
```

In this case, the constructor takes in five different arguments (name, breed, weight, eyeColor and hairColor).

So, when an object is created, it has those specific attributes or qualities.

</div>
</div>
<div id="Video" class="tabcontent">

<div class="tabhtml" markdown="1">

<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/8P2MauS9HVQ" frameborder="0" allowfullscreen></iframe></div>
</div>
</div>
