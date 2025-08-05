---
layout: post
title: Blender hardlight vs softlight in 2 min
date: 2025-06-08
categories: blender
author: insane
permalink: /posts/blender-hard-light-vs-soft-light-in-2min
tags: blender lighting 3d
---

![Thumbnail for the post](/assets/blender-hardlight-vs-softlight-in-2min/thumbnail.webp)

When we render a model in blender we can have at the most basic two types of lighting – Hard lighting and soft lighting which determines how harsh or soft the shadows are.

In hard lighting the bright areas appear very bright and dark areas (shadows appear harsher) appear very dark compared to soft lighting (shadows appear softer). Lets use point light source for example. If we use increase the radius of the light then it would be soft lighting and if we would decrease the radius of the light source it would be hard lighting.

- In hard lighting – shadows are harsh
- In soft lighting – shadows are soft

Here we can see when the radius of the light source is 0 the shadow seems to be very harsh on the object.

|                                                               Model                                                               |                                                                                                  Properties                                                                                                  |
| :-------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| ![A 3D model in blender with hard lighting applied to it](/assets/blender-hardlight-vs-softlight-in-2min/blender-hardlight.webp) | !["Light properties panel with point light set to 40 W power and 0 m radius, used to create hard lighting on the 3D model"](/assets/blender-hardlight-vs-softlight-in-2min/blender-hardlight-properties.webp) |
|                                                                                                                                   |                                                                                                                                                                                                              |

However when the radius is increased to 0.39 we can see the shadows become much softer.

|                                                               Model                                                               |                                                                                                   Properties                                                                                                    |
| :-------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| ![A 3D model in blender with soft lighting applied to it](/assets/blender-hardlight-vs-softlight-in-2min/blender-softlight.webp) | !["Light properties panel with point light set to 40 W power and 0.39 m radius, used to create soft lighting on the 3D model"](/assets/blender-hardlight-vs-softlight-in-2min/blender-softlight-properties.webp) |

**Extra:** For the same radius changing strength of the light source would also determine how much hard or soft the lighting is. More the strength harder the lighting, lesser the strength softer the lighting.

And that's it!

🦖