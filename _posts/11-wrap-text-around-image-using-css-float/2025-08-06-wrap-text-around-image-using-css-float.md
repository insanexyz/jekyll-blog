---
layout: post
title: Wrap text around image using CSS Float
date: 2025-08-06
categories: css
author: insane
permalink: /posts/wrap-text-around-image-using-css-float/
tags:
  - css
  - float
  - html
  - webdev
---

![Thumbnail for the post](/assets/wrap-text-around-image-using-css-float/thumbnail.webp)

I have made made a `<div class='box'>` and inside it is a `<img>` element and `<p>` element with some text. `<div class='box'>` as a black border with 10px padding, `<img>` has a red border and `<p>` has a green border. I have also reset global `(*)` css margin and padding to 0.

Currently the text simply goes below the image. Default behavior of block level elements.

```html
<html>
    <head>
        <title>CSS Float</title>
        <style>
          <!-- 
            I have not added the css for adding borders and all as it is very 
            simple to implement, and will make the code long for no reason.
          -->
        <style>
    </head>
    <body>
        <div class="box">
            <img src="guts.jpg" width="230px" />
            <p> ... </p>
        </div>
    </body>
</html>
```

![A main div with class=box with a image element and paragraph element inside it. No css float is applied to the image so the paragraph element simply goes below the image.](/assets/wrap-text-around-image-using-css-float/css-no-float.webp)

Now to make the text wrap around the image, add `float: left` to `<img>`. The image will then floats on the left, and text wraps around it.

```html
<html>
    <head>
        <title>CSS Float</title>
        <style>
            .box img {
                float: left
            }
        <style>
    </head>
    <body>
        <div class="box">
	        <img src="guts.jpg" width="230px" />
            <p> ... </p>
        </div>
    </body>
</html>
```

![CSS float applied to the image so the paragraph element's text wraps around the image.](/assets/wrap-text-around-image-using-css-float/css-float-with-no-padding-no-margin.webp)

You will notice that image is actually floating inside `<p>`'s border. Add some margin to `<img>` to notice it.

```html
<html>
    <head>
        <title>CSS Float</title>
        <style>
            .box img {
                float: left;
                margin: 10px;
            }
        <style>
    </head>
    <body>
        <div class="box">
            <img src="guts.jpg" width="230px" />
            <p> ... </p>
        </div>
    </body>
</html>
```

![Margin of 10px is added to the image element to depict it is floating inside paragraph element's border.](/assets/wrap-text-around-image-using-css-float/css-float.webp)

The image being big overflows `<div class='box'>`  border. One simple way to fix it is to add `display: flow-root` to the `<div class='box'>` .

```html
<html>
    <head>
        <title>CSS Float</title>
        <style>
            .box img {
    			float: left;
    			margin: 10px;
    		}
    		
            .box {
                display: flow-root;
            }
        <style>
    </head>
    <body>
        <div class="box">
            <img src="guts.jpg" width="230px" />
            <p> ... </p>
        </div>
    </body>
</html>
```
![display: flow-root applied to div with class=box so image doesn't overflow it.](/assets/wrap-text-around-image-using-css-float/flow-root-applied.webp)

Now add some more text to `<p>` to see more wrapping.
![More text added to the paragraph element to show proper wrapping of its text around the image.](/assets/wrap-text-around-image-using-css-float/more-text.webp)

Now a days we use grid or flexbox to achieve the same.

:p