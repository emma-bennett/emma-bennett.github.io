---
layout: post
title:  "formatting your jekyll theme (part 2)"
date:   2020-06-03 12:00:00 -0400
tags: [jekyll website design]
excerpt_separator: <!--more-->
---

Now, once we have a fully functioning website there are a couple steps to take to customize it to become your own. There are going to be multiple different folders which Jekyll uses to organize the different elements of your website. <!--more--> 
In this post, I'll be walking you through the main components of a Jekyll website (Remember that this may vary slightly based on which theme you have chosen for yourself).

<h4>1) _Config.yml </h4>
This file should include all of the customization of your home page.

{% highlight ruby %}
title:
email: 
description: >- # this means to ignore newlines until "baseurl:"
  home
baseurl: "" # the subpath of your site, e.g. /blog
url: "" # the base hostname & protocol for your site, e.g. http://example.com
header_text:
header_feature_image: 
{% endhighlight %}

Most of these are self-explanatory. The header_text and header_feature_image are quite cool. This is specifically for the type-on-strap theme I use where a huge banner lays across your screen and you can change the image or the text displayed on it.

<h4>2) Layouts and Includes</h4>
Layouts are the base of your website. Some different layouts may include your home page, a page that displays all of your posts, or the page that includes a search bar. Layouts take bits and pieces of _includes html files in order to piece themselves together. The example below is for a normal page that displays all posts on it. The actual code for "blog.html" is not shown, but the code is meant to show how a layout html page interacts with an _includes html page.
{% highlight ruby %}
---
layout: default
---

include blog.html
{% endhighlight %}

Most layouts rely on bits of _includes html files in order to display. Includes files are like the header, footer, each post, search bar, etc. All of your other files rely on these include files to get their html and css from. The example below displays the _includes code for a portfolio page.
{% highlight ruby %}
{% include portfolio.html %}
{% endhighlight %}

<h4>3) Posts</h4>
Posts are in their own folder. When you add another markdown file to the folder with the correct post formatting, Jekyll automatically adds this file to your collection of posts.
{% highlight ruby %}
layout: post
title:  ""
date:  
tags: # tags you put here are the tags which this post would be listed under in the tags section
excerpt_separator: <!--more-->
{% endhighlight %}
A really smart aspect of posts that Jekyll includes is the excerpt separator. This allows you to place a marker of where you want the excerpt of your post (shown on the home page) to end.

<h4>4) Pages</h4>
Pages are the tabs that show up at the top of your webpage. Examples are projects, search, tags, etc. They are quite simple to set up, only needing the layout, name, and possibly a feature image.
{% highlight ruby %}
layout: page
title: about
permalink: /about/
feature-img: ""
{% endhighlight %}
