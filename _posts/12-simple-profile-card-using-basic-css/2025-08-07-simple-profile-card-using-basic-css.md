---
layout: post
title: Simple profile card using basic CSS
date: 2025-08-07
categories: css
author: insane
permalink: /posts/simple-profile-card-using-basic-css/
tags:
  - css
  - html
  - webdev
  - profile-card
  - post-12
---

![Thumbnail for the post](/assets/simple-profile-card-using-basic-css/thumbnail.webp)

<br>

Code -
```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Document</title>
        <style>
            @import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

            * {
                margin: 0;
                padding: 0;
            }

            .card * {
                margin-bottom: 10px;
            }

            .card {
                font-family: "Poppins", sans-serif;
                font-weight: 400;
                font-style: normal;
                font-size: 10px;
                background-color: white;
                border-radius: 10px;
                width: 350px;
                padding: 10px;
                box-shadow: 0px 0px 10px 0px grey;
                margin: 50px auto;
            }

            img {
                border-radius: 10px;
                height: 300px;
                width: 350px;
            }

            .tag {
                margin-left: 5px;
                margin-bottom: 30px;
            }

            .tag span {
                box-shadow: 0px 0px 5px 0px grey;
                padding: 5px;
                border-radius: 10px;
                font-size: 1.2em;
            }

            .tag span:nth-child(2) {
                margin-left: 5px;
            }

            .card h1 {
                margin-bottom: 15px;
                font-size: 3.5em;
            }

            .card .content p {
                font-size: 1.5em;
            }

            .card a {
                text-decoration: none;
                box-shadow: 0px 0px 2px 0px grey;
                border-radius: 25px;
                display: block;
                width: max-content;
                margin: 0 auto;
                margin-top: 30px;
                padding: 10px;
                background-color: lightcyan;
                color: blue;
                font-size: 1.2em;
                cursor: pointer;
            }

            .card a:hover {
                background-color: lightblue;
            }
        </style>
    </head>
    <body>
        <div class="card">
            <div class="image">
                <img src="image.jpg"
                    alt="cover image"
                />
            </div>

            <div class="tag">
                <span>Coder</span>
                <span>Coder</span>
            </div>

            <div class="content">
                <h1>About me</h1>
                <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                    Laborum, dolores error fuga autem voluptatum nam? Unde illum
                    veritatis consequuntur quo est a similique quibusdam, iure,
                    error ducimus, delectus sint sed?
                </p>
            </div>

            <a href="#">Read more</a>
        </div>
    </body>
</html>
```

![](/assets/simple-profile-card-using-basic-css/profile-card.webp)