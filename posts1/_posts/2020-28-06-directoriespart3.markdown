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
  
{% highlight ruby %}
"for post in site.portfolio"
#surround the above statement with % signs
{% endhighlight %}
  
  What this does is it says to format each of the posts in a specific posts
  directory (in this case posts1).
  
  *coding tid-bit* - the above format actually follows that of a for-each loop where it looks at every object in the
   'site.portfolio' folder and formats each into its own blog post.
   
The upside to having multiple different directories is that they all still work in the search bar and also work as
 their own filtered tags automatically, but it is easier to accumulate more alike posts together on the same page.
 
 Hopefully you are now comfortable creating different Jekyll directories! Thanks for reading.