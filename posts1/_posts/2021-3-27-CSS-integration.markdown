---
layout: post
title:  "CSS integration"
date:   2021-03-27
tags: [jekyll website design]
thumbnail: "img/cssblog.jpg"
excerpt_separator: <!--more-->
published: true
---

This article will discuss the basic knowledge needed in order for one to integrate CSS into bits of an HTML page. Examples include having an image fade in or having text slide onto the screen from right-to-left.

<b>Let's start with the basics: Where exactly in your HTML file should your CSS reside?</b>

An HTML file uses the {% highlight ruby %} <style> {% endhighlight %} tag to store the information on how HTML
 elements should render on your website. Within this style tag is where the values (color, size, font, etc.) you want
  to change should be declared.

