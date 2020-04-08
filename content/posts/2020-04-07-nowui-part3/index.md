---
title: "Now Experience Part 3: Wasn't I Meant To Be A ServiceNow Developer?"
summary: "Maybe? 🤷‍♀️"
date: 2020-04-07T10:17:14+10:00
draft: true
toc: false
tags: 
  - Now Experience
  - ServiceNow
---

If you have been following along with [my](./../2020-03-20-nowui-part1) [blog](../2020-03-24-nowui-part1point5/) [series](../2020-03-26-nowui-part2/) on the Now Experience (Congrats if you have! :tada::tada: I know it's a long read), you may have started thinking to yourself, or yelling out loud into the void "BUT WHAT ABOUT SERVICENOW? WHAT ABOUT THE PLATFORM? WHERE IS MY INSTANCE? WHY DO I EXIST!?" and I want you to know, **you are heard**. 

This post I'm going to talk a little about how to get your components to your instance, but I'm also going to digress **A LOT** and talk more broadly about what the Now Experience means, and if you are *really* going to have to learn it for your career. (HINT: Maybe?)

## Publishing Your Component

So you have "Hello"'d the  :earth_asia:with a :wave:- Now we want to see that in our Instance. Luckily, our old friend the Now-CLI has that in hand. 

Make sure you have logged into your instance (follow the steps in [Part 1](../2020-03-26-nowui-part1)) and give the CLI the magic command: `now-cli deploy`. 

You should see something like this:
![Deploy 1](deploy1.png)

The things to note are the lines in green: 
```
Creating 4b8ec5da08d47d55cd6a57f11a4552ab in sys_ux_lib_source_script
Creating 331b5f9d4137b1361b099ecf2aa4386b in sys_ux_lib_component
```


## Hard Chat