+++
title = "Hello World"
summary = "A new website, a new blog, hopefully a new enthusiasm for writing!"
tags = [
    "Blog",
    "Personal",
]
date = "2019-12-10"
toc = true
+++

## Hello World. This is the new internet.

I have been meaning to update my personal website ever since I realised crappy HTML and a Wordpress blog stopped me from really enjoying writing and web design. I have also been rather busy with work and having two (2!) kids.

<!-- more -->

The new blog and website also meant I needed to knuckle down and learn some web technologies that I had been hearing about for a long time, but never really exposed myself to: 
- Git & Github
- NodeJS 
- Vue
- Markdown

It started about a year ago when I was looking at AngularJS, Angular, React and read about a new plucky up-and-coming web framework called Vue. I don't really know much AngularJS, Angular or React, and Vue seemed like a much quicker, easier to learn and more lightweight javascripty-thing that I would come to learn is a "Front-End Framework". 

After I decided I wanted to get to know Vue, the next step was looking at a way to use it to update my site and blog. I did some googling and found Ghost CMS (Vue based Hybrid/Headless CMS) and tried to have a play with that, but my old shared web hosting isn't the best with Node apps. So that lead me to VuePress. 

## VuePress
VuePress is a Vue-based Static Site Generator designed for quickly building Documentation sites for other tools. It had me interested because it claimed to be *very* fast, SEO compliant and quick to set up. You also don't need to know Node or Vue out of the box to get something working. That suited me perfectly.

The next question was, how do I blog in it?

## VuePress-Blog
So sure enough, there is an official plugin for VuePress which lets you ("somewhat") easily create blog posts as Markdown files and render them into a Post / Tag / Dated hierarchy. Again, sounds perfect, but it wasn't as easy as I had hoped. 

The docs are pretty light-on, and some of the issues I was trying to fix (VSSUE Comments, themeing, layouts) I could only work out by finding the github repo of someone else who had set up a blog using this plugin. But, in the end, I got there, and now you are reading it. 

There are some really cool features in Markdown and VuePress. I love being able to drop code `in-line like this` or in blocks 
```javascript
var x = likeThis();
```
I also love that it's taught me to use Git and write in Markdown.

## What's next?

The website will continue to improve as I find time to fix it, and (hopefully!) get to learn Vue `spoiler from the future - It doesn't!`. I also have some plans for creating some really cool ServiceNow content and sharing it with the world.

Thanks for sticking with me! Catch you next post ;)
  
`- Andrew`