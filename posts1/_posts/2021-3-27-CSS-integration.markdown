---
layout: post
title:  "CSS integration"
date:   2021-03-27
tags: [jekyll website design]
thumbnail: "img/cssblog.jpg"
feature-img: "img/cssblog.jpg"
excerpt_separator: <!--more-->
published: true
---

This article will discuss the basic knowledge needed in order for one to integrate CSS into bits of an HTML page. Examples include having an image fade in or having text slide onto the screen from right-to-left.

<b>Let's start with the basics: Where exactly in your HTML file should your CSS reside?</b>

An HTML file uses the tag below to store the information on how HTML
 elements should render on your website. Within this style tag is where the values (color, size, font, etc.) you want
  to change should be declared.

{% highlight ruby %} <style> here is where you would add any CSS code </style> {% endhighlight %}

<br>
<b> So now that we've covered where the CSS resides, how is it formatted and implemented? </b>

For more straight-forward things like transforming text and margin height you use the name of the item (p, h1, h2
, etc.) that you want to modify and in curly brackets put all of the different 'transformations'. An example is shown
 below:
 {% highlight ruby %}
  h1{
   text-align: center;
   text-transform: uppercase;
   color: #4CAF50;
    margin-top: 0px;
    margin-bottom: 0px;
 }
 {% endhighlight %}

