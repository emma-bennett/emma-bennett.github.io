---
layout: post
title:  "creating jekyll post directories (part 3)"
date:   2021-02-03
tags: [jekyll website design]
thumbnail: "img/directories.jpeg"
excerpt_separator: <!--more-->
published: true
---
<b>What do you do when you want two post directories so only select posts show up on certain places on your site: </b>Post directories.
<!--more-->

See an example of this in my <i>Series/Comp Sci Tutorials</i> and in my <i>Posts</i>.

The easiest way to do this?
Let's imagine a scenario. You want one page to display posts about Topic A and the other page to display posts about
 Topic B.
1.  Put .markdown posts of Topic A in a folder called posts1 and the others in another folder called posts2.
2.  Within the _includes files (where the html of how your individual pages are generated resides), add a line to the
 top that specifies where you want your page to get its posts from.
 
     The line to add is the following:
     
     "{% for post in site.categories.posts1 %}" 
       
     What this does is it says to format each of the posts in a speicifc posts directory (in this case posts1).
