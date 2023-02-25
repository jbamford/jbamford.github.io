---
layout: post
title:  "MagicMirror Custom Module (MMM-PenPlotter)"
date:   2023-02-25 12:31:56 -0400
categories: projects
---


## An overview of the library and its features

[Github-MMM-PenPlotter](https://github.com/jbamford/MMM-PenPlotter)

I enjoy watching pen plotting and Sandify pictures come to life. It's fascinating how a simple line can create such a mesmerizing image that captures your attention. I started thinking about how I could recreate this effect on my Magic Mirror. The idea of a line being drawn and coming to life through the mirror seemed like the perfect way to make the mirror more of an art piece than a cool tech project.

Fortunately, MagicMirror offers the ability to build new modules Docs. To achieve the illusion of a line being drawn, I explored several common plotting javascript libraries. However, I eventually settled on using an SVG file format as it proved to be the most effective and lightweight solution, even when plotting over 10,000 points

To start, I modified https://github.com/AdamMoses-GitHub/MMM-ImageSlideshow package to start as the base of my project.

The library accepts a folder of images and rotates through them for a preset amount of time. 

In general, the MMM-PenPlotter module is designed to display SVG animations. The SVG files are animated using CSS. The animation progressively draws a white line on a black background until it completes the entire SVG path. This creates the illusion that the line is magically rendered on the mirrored glass.

### SVG 
Given a single SVG path you can animate the path to look like its being drawn, by adjusting the stroke-dasharray with keyframes(helpful article). The issue with the MMM module was I couldn’t figure out how to run the required javascript code to calculate the length of the SVG path, and update the stroke-dasharray dynamically based on a random SVG input. The only way the animation would render on the mirror was if you set the <style> properties of the SVG using the already precomputed length values. 

My process was as follows:
 - Make a Penplotting SVG (link)https://sandify.org/
 - Download the file and check its length.
 - Add a style tag in the svg file itself with the updated ​​stroke-dasharray values. 
    - This way whenever the SVG file was opened it would auto-animate itself no Javascript required.
 - Update the SVG background to black and the line to white

It turns out: that you do not need to calculate the length of the SVG each time. You can just set the SVG length to “1”. This way your key_animation will always be the same regardless of how complicated the SVG is(mind blown when I figured this one out), and it saves a lot of time building the SVGs.

### Project Inspiration 
Sisyphus, PenPlotters(in general), and https://www.youtube.com/watch?v=7i78DSaMhls