---
title: "Now Experience Part 2: Let's Build a Thing"
summary: "Knowledge Without Action is Futile... or so I've heard"
date: 2020-03-26T20:00:00+10:00
draft: true
toc: true
images:
tags: 
  - ServiceNow
  - Now Experience
---

Welcome to my third blog post on the Now Experience. Part 2. Yes, I know it's confusing. If you haven't, check out [Part 1](../2020-03-20-nowui-part1) and/or [Part 1.5](../2020-03-24-nowui-part1point5) before continuing. We are going to cover a lot here, but not what has already been covered :smile: 

For those joining us here, you'll need the following:
- An environment set up to run the [Now-CLI](https://docs.servicenow.com/bundle/orlando-servicenow-platform/page/build/components/task/set-up-environment.html) with my settings from [Part 1](../2020-03-20-nowui-part1)
- VS Code and Git (optional, but c'mon, don't be like that)
- An understanding of Javascript and ServiceNow
- A ServiceNow Instance on the Orlando Version (Guide for your FREE PERSONAL INSTANCE [HERE](https://developer.servicenow.com/dev.do#!/learn/courses/orlando/app_store_learnv2_buildmyfirstapp_orlando_build_my_first_application/app_store_learnv2_buildmyfirstapp_orlando_servicenow_basics/app_store_learnv2_buildmyfirstapp_orlando_personal_developer_instances))

We will be creating a basic component, and I'll be running through the WHAT and WHY of what's going on in more detail. 

Now (haha, like the Experience, and the platform...) Let's get cracking!

## Getting Cracking

I think it's only fair to start at the beginning, and utilise what our friends at the ServiceNow [Developer Program](https://developer.servicenow.com) have made and hit up the [first example](https://developer.servicenow.com/dev.do#!/guide/orlando/now-experience/ui-framework/examples/counter) which is a simple Counter app. We might *zhoosh it up* a bit by using an Out of the Box button, but we'll see how we go :wink:. 

### Step 1: Make a Place and Init That Git! 

In your "projects" directory, create a new folder called something like "example-component-counter" sticking to that "Kebab-case" we mentioned in my previous blog. Open that up in Visual Studio Code and follow the steps from my last blog:

- Open the folder in VS Code
- Switch to the Source Control tab and hit the big *Initialize Repository* button
- Open the Terminal in VS Code by going "View / Terminal" or Ctrl+`

> HOT TIP: Using the terminal in VS Code is awesome, because it's already pointed to the folder you have open, and it keeps everything together! You will see how useful this is shortly.

### Step 2: Loggity Inn

We need to log in to our instance via the CLI to allow it to validate everything as we BUILD STUFF. 

In the terminal, type:

`now-cli login --host "https://your-instance.service-now.com" --username "your-username" --password "your-password"`

You should get a tick, and a note about saving the credentials. Something like:
![CLI Login](cli1.png)

> This login can be OAuth I think, but, no, I'm not helping with that soz :wave:

### Step 3: Understand, and Scaffold

The next step is using the CLI to "Scaffold" our new project. BUT... and there's always a :peach: - We need to know what we want to make.

The [Dev Docs](https://developer.servicenow.com/dev.do#!/guide/orlando/now-experience/cli/now-cli/) lay out a few things we need to know first:

- We need a `Name` (The bane of Developers)
  - This *should* be a "Valid and Unique" [NPM package name](https://docs.npmjs.com/files/package.json). This is a guideline if you plan on sharing your component to the greater community, and may or may not be super critical. Let's just stick with it for now. I'm going to use my initials and package name e.g. `@aad/mypackage`
- We need a `Description` (A bit easier)
- We could also specify a `Scope` (The ServiceNow one)
  - This is limited to 18 characters, and is validated against the instance you have logged in to
  - Must follow the form x_customerprefix_componentname - MORE ON THIS SOON
  - If you leave it blank, it'll generate one for you. Let's do this for simplicity

> EXTRA CREDIT: To find your Customer Prefix - Check the System Property in your instance here: 
> ```
> https://your-instance.service-now.com/nav_to.do?uri=%2Fsys_properties.do%3Fsys_id%3D8fc888b2d77311004f6a0eca5e6103e6
> ``` 
> under the "Value" field

We are going to use the name `example-component-counter` as that's what we called our folder.

Now we MAKE SOMETHING: Create your component "Scaffolding" using the Now-CLI by running the following command in the VS Code terminal:

 `now-cli project --name "@aad/example-component-counter" --description "It's what it says on the lid"`

You should see a bunch of text go flying by, and a few notes like "Scaffolding Complete!" and "blah blah do stuff blah blah". You will also note, if you are paying attention, that a WHOLE MESS OF CRAP just landed in our directory! That's your new component!

![CLI 2](cli2.png)

### Step 4: What just happened?

### Step 5: Blah Blah Do Stuff Blah Blah

### Step 6: Let's make something appear!

### Step 7: Oh yeah, that's right, I'm meant to be a ServiceNow Developer

### Step 8: Push that Git

