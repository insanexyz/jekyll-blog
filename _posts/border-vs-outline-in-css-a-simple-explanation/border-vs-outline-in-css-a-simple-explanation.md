---
layout: post
title: Border vs Outline in CSS – A Simple Explanation
date: 2025-07-17
categories: webdev
author: insane
permalink: /posts/border-vs-outline-in-css-a-simple-explanation/
tags:
  - html
  - css
  - border
  - outline
  - post-08
---

![Thumbnail for the post](/assets/border-vs-outline-in-css-a-simple-explanation/thumbnail.webp)

Border and outline are two ways to add borders around an element in HTML/CSS.  
But they don’t behave the same.

Border **respects margins** between two elements and never spills out.  
On the other hand, an **outline** doesn’t care about margins — it can **overflow** and bleed into other elements.

---

Let us understand this with a simple example:

Here I have created two ``<div>s`` box1 and box2 having a space (margin) of 10px between them.

```html
<!doctype html>
<html lang="en">
    <head>
        <title>Document</title>
        <style>
            * {
                margin: 0;
                padding: 0;
                margin: 10px;
            }

            .box1 {
                outline: 1px solid black;
            }

            .box2 {
                border: 1px solid black;
            }
        </style>
    </head>
    <body>
        <div class="box1">Box 1 uses outline</div>

        <div class="box2">Box 2 uses margin</div>
    </body>
</html>
```
![Two divs box 1 and box 2. Box 1 has 1px solid black outline and box 2 has 1px solid black border. Both have a space (margin) of 10px between them.](/assets/border-vs-outline-in-css-a-simple-explanation/border-vs-outline-default-with-marker.webp)

---

Now, no matter how much I increase the **border** size in box2, the spacing between the two elements is still maintained.  
Here I increased the border size to 50px and space between the two boxes is still maintained.

```html
<style>
    * {
          margin: 0;
          padding: 0;
          margin: 10px;
      }

      .box1 {
          outline: 1px solid black;
      }

      .box2 {
          border: 50px solid black; /* Border size increased to 50px */
      }
</style>
```
![Two divs box 1 and box 2. Box 1 has 1 px solid black outline. Box 2 has 50 px solid black border. The space of 10 px between them is retained.](/assets/border-vs-outline-in-css-a-simple-explanation/border-size-increased-with-marker.webp)

---

But when I increase the **outline** size in box1 to 15px, it simply ignores that 10px space and **overflows** into box2. (Extra: Yes 5px bleeds into box2 from box2’s upper border)

```html
<style>
    * {
          margin: 0;
          padding: 0;
          margin: 10px;
      }

      .box1 {
          outline: 15px solid black; /* Outline size increased to 15px */
      }

      .box2 {
          border: 1px solid black;
      }
</style>
```
![Two divs box 1 and box 2. Box 1 has 15px solid black outline. Box 2 has 1px solid black border. The space of 10px between them is not retained.](/assets/border-vs-outline-in-css-a-simple-explanation/outline-size-increased.webp)

---

Same thing happens when outline-offset property of box1 is increased.  
  
**Note:** Outline offset simply controls how far the outline is pushed **outward or inward** from its default position.

```html
<style>
    * {
          margin: 0;
          padding: 0;
          margin: 10px;
      }

      .box1 {
          outline: 15px solid black;
          outline-offset: 15px; 
          /* Outline-offset property set to 15px. Default value is 0px. */
      }

      .box2 {
          border: 1px solid black;
      }
</style>
```
![Two divs box 1 and box 2. Box 1 has 1px solid black outline and 15px outline-offset. Box 2 has 1px solid black border. The space of 10 px between them is not retained](/assets/border-vs-outline-in-css-a-simple-explanation/outline-offset-increased.webp)

---

End. <br>
🦖