---

layout: post
date:   2020-05-11 19:40:00 -0400
title: setting up jekyll-based theme (part 1)                                # Title of the page
feature-img: "img/commandprompt.jpg"                        # Add a feature-image to the post
thumbnail: "img/commandprompt.jpg"
tags: [jekyll website design]
excerpt_separator: <!--more-->

---
This is my first website using the Jekyll plug-in. I'll be walking you through the steps to create a fully-functioning website using a Gem-based theme. On this particular website I used the [type-on-strap theme](https://github.com/sylhare/Type-on-Strap).

<!--more-->
Things you need:
* access to a command prompt
* [Ruby environment](https://jekyllrb.com/docs/installation/)


Now you're going to want to install Jekyll and bundler gems to your Ruby environment. You can do this by going to the command prompt and typing in the following:

{% highlight ruby %}
gem install jekyll bundler
jekyll new myblog
cd myblog
bundle exec jekyll serve
# Browse to http://localhost:4000
{% endhighlight %}

This should set up a website using the default jekyll theme: minima. Upon looking into the folder you created in your directory named "myblog", pay close attention to two files: 1) _config.yml 2) Gemfile

Now, we are going to browse for a theme. [Jekyll Themes](https://jekyllthemes.io/free) allows you to browse through a multitude of free themes.

![Jekyll Theme](/img/jekyllthemepreview.png){:class="img-responsive"}

Here, you can scroll through multiple demos of these themes and find one that you like. Let's say I like the theme type-on-strap. Go to [rubygems.org](https://rubygems.org/) and search for the theme that you want.

A screen like this should show up. The code I circled is what you should substitute for in your Gemfile (gem "type-on-strap"). In your _config.yml file you should substitute "type-in-strap" instead of "minima" after the "theme:".
![Gemfile install](/img/themegemfile.png){:class="img-responsive"}


Finally, look at the command I circled below to get an idea of what to put in your command prompt. Find the folder "myblog" in your directory and under it enter in the code circled. This should install the theme you want.
![Theme install](/img/themeinstall.png){:class="img-responsive"}

Now when you go to your local host you should see your website with your newly installed theme. Thanks for reading!
