---
layout: ../../layouts/MarkdownPostLayout.astro
title: 'miniRT: Supposed to be mini'
pubDate: 2026-02-XX
description: 'Raytracing is a deeper rabbit hole than I thought'
author: 'Aisling Fontaine'
tags: ["42", "raytracing", "C/C++"]
---

One of the big(ger) projects at 42 is left for you to choose: either a 3D game using ray casting, or a minimal raytracer.
Either way, you'll have to code it using C98, no external libraries aside from the pile of steaming garbage that is the MiniLibX.
Basically a wrapper for the X windowing system, so it's really basic and you can't do much by default.
Thankfully, for the project me and a friend chose to build, we only had to draw pixels; the rest wasn't relevant to the library.

\<image here>

## Tracing Rays
Let's start from the beginning: **what even is ray tracing to begin with?**

Ray tracing is the process of determining what color to print on your screen by launching rays through your camera. Let me explain.

\<image here showing the sending through camera pixels process>

Your screen has pixels, right? Well, when *rendering* a scene in three dimensions, each of your pixels has to have a color
representing the object you're looking at. How are those colors calculated in practice? The idea is simple:
**trace a straight line from your point of view (through the pixel), and see the first object that it reaches: that object's color is your pixel's color**.

Now of course, in practice this gets way more complicated. You have to take into account the lightning conditions, reflections and all that good stuff.
I might do an article on all of these concepts one day. For now, have a few cool screenshots:

\<screenshots here>

This project was a lot of fun to build, and we learned so much on building real applications in C.

The next project is an HTTP web server, which is going to be another beast altogether, especially considering
the language we have to build it with: C++98.

Have a great week-end!

~ash
