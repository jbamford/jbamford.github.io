---
layout: post
title:  "How To Animate SVGs"
date:   2023-03-26 12:31:56 -0400
categories: projects
---

## SVG’s With One Path Attribute 

1. Download an SVG File 
    1. I like to use this website however there are many out there. 
        1. [https://sandify.org/](https://sandify.org/) (most of the svgs in the [repository](https://github.com/jbamford/MMM-PenPlotter/tree/main/example_svg) came from here)
        2. [https://drawingbots.net/knowledge/tools](https://drawingbots.net/knowledge/tools) a nice collections of tools
    2. Be sure to download the file as an SVG

<p align="center">
<img src="/images/export-from-tool.png" alt="drawing" width="350" style="center"/><br>
</p>   

2. Open the SVG in a text editor 
    1. In the text editor make the background black
    2. Adjust the path attributes
        1. class="path"
        2.  stroke="white"
        3. stroke-width="0.2mm"
        4. fill="none"
        5. pathLength="1"
   
   <p align="center">
<img src="/images/path-atts.png" alt="drawing" width="350" style="center"/><br>
</p>
    5. Add in the Style Tag to force the animation magic 
        1. You want to add the animation in the style tag in order to avoid having to use any javascript
         
{% highlight css %}
 <style>
        path {

            stroke-dasharray: 1;
            stroke-dashoffset: 1;
            animation: draw 60s linear forwards;
          }
          
          @keyframes draw {
            from {
              stroke-dashoffset: 1;
            }
          
            to {
              stroke-dashoffset: 0;
            }
          }

          @-webkit-keyframes draw {
              to {
                  stroke-dashoffset: 0;
              }
          }          
          
    </style>
     
 {% endhighlight %}
   <p align="center">
<img src="/images/style-info.png" alt="drawing" width="350" style="center"/><br>
</p>     
     
1. Save your edits and your newly minted SVG to your mirror’s SVG folder

## SVG’s With Multiple Path Attributes 

But wait, Jason, the SVG I downloaded has multiple paths in it… See [a video here](https://youtu.be/Nz0SzKKdd-A) where I walk through the process of animating an SVG of a map that has many path elements. The final results look like the city is being drawn. 

1. Update all the Path attributes to have a pathLength="1"
2. Note how many path attributes there are in the file
3. Input the number of paths in the file into the [generate_style.py](https://gist.github.com/jbamford/964e6e3ad1dd8afd17507e2ce70eff94) file
4. Save the output from generate_style.py and paste it into a new &lt;style> paste_here &lt;/style>
5. Check that the Fill is either none or black, and that the stroke is white. 

<p align="center">
<img src="/images/Scranton.svg" alt="drawing" width="350" style="center"/><br>
</p>   