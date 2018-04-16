---
layout: single
title:  "Home page complete"
date:   2017-07-07 10:04:58 +0100
categories: blog setup
excerpt: "in this post i write about my journey in completing this site"
---
Nothing comes easy as they say. I have been working on setting up my jekyll based site.

In another post I will detail how I began and completed the whole set up.
The purpose of this post is just to celebrate this victory in setting up the basics

I installed a gem based jekyll theme called [minimal-mistakes](https://mmistakes.github.io/minimal-mistakes/) and loved the layout and the idea that it also offered a display of a _portfolio_ of sorts. 

With a little ideas borrowed from another theme I ended up doing a mash up of both themes to come up with my current layout for my landing page. Its a nice combination.

My page features a large header image and a "call-to-action" button which prompts my guests to contact me if they need me to work on any of their projects. This is how it looks: 

![home header image](/assets/home-header.jpg)

Next up I added a portfolio previewer which I sort of borrowed from the other theme.

One thing I appreciated in my learnings while setting up this site was the versatility of Sass. It makes CSS very easy to manage and all that. 

Take for instance when I wanted to copy the styling of the contact form and the portfolio profiler. All I had to do was simply copy the sass files with file extension `.scss` from the themes sass folder and then import them into my main themes main sass files. Voila!

It was as easy as three to four lines of sass:
{% highlight sass linenos %}
@import "minimal-mistakes/1-colors"
@import "minimal-mistakes/1-mixins"
@import "minimal-mistakes/1-vars"
@import "minimal-mistakes/3-contact"
@import "minimal-mistakes/3-work"
{% endhighlight %}

It was an exiting experience figuring out how this jekyll based static sites work and setting up my website and blog in the process. This is one of the first of my many posts on this blog. I hope to keep it up-to-date with relevant information about my findings and also my learnings in the world of web-development.