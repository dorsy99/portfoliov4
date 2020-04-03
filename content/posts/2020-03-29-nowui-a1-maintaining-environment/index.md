---
title: "Now Experience Addendum 1: Maintaining Your Environment"
summary: "It's like a garden, but instead of bugs it's... well it's still bugs."
date: 2020-04-02T21:00:00+10:00
draft: false
toc: false
tags: 
  - ServiceNow
  - Now Experience
---

If you have been following [my blogs](/tags/now-experience/) on the Now Experience so far, you'll have noticed they are getting longer. A couple days ago ServiceNow updated the Now-CLI to version 17.0.2 - which is "point-oh-one" more than the version we installed in [Part 1](../2020-03-20-nowui-part1). So, let's stop to look at keeping your local development environment up to date!

> Package Managers help you update stuff as easily as they install, BUT (And there's always a :peach:) they will only do what you (or your **package.json**) tells them to do.

So, let's understand the 3 levels of things we might need to update:

1. Our OS-level applications (like Node, or your package managers Homebrew/Chocolatey & NPM themselves)
2. Your global NPM packages (Like Now-CLI)
3. The dependency packages installed in your project

Alright then, we want to make sure our Package Managers (in my case, Homebrew and NPM) are up to date. Most package managers are command line so :fire:Fire up those terminals!

> HOT TIP: Some package managers have two commands that are similar, but different: "`update`" and "`upgrade`". 
> 
> **Update** is usually INTERNAL, to update the package manager itself, and it's list of packages from the repository it connects to.
> >
> **Upgrade** is to update a version of a package it is managing.   
> >
> If you aren't sure, you can run the help command e.g. `brew upgrade --help` for more information. To further confuse things, in NPM update and upgrade are the same, you just call the command on itself to update it.

Run the command `brew update`. Homebrew will check with it's repository and show you any new, updated and removed formulae. Then, you can run `brew upgrade` to update any of your packages which might need it.

Once that's done, let's do the same with **NPM**. Remember there is "Global" NPM packages, and Local one. We want to update our Global packages (specifically, for us, the Now-CLI). Run `npm update -g` and NPM will give you a quick note about what changed: 

```
+ npm@6.14.4
added 9 packages from 5 contributors, removed 4 packages and updated 29 packages in 4.352s
```

> If you just want to update Now-CLI you can run `npm update -g @servicenow/cli` directly.

You should now have the latest version of the Now-CLI - test by (you guessed it) running `now-cli --version`. It should come back as 17.0.2 (as at 1st April, 2020).

Finally, we want to make sure all the packages and dependencies we installed to run our components are up to date as well.

Navigate to your component directory in terminal (Or use the built in one from Visual Studio Code) and run `npm update`. If there is nothing to update, nothing will happen. 

> HOT TIP: NPM respects information in the **package.json** file in relation to dependency versions. These can include special characters to let you know what minor patches and versions dependencies can include. for example, one line in our package.json is `"@servicenow/ui-effect-http": "^17.0.1"` - The `^` implies that it could update to `17.1.0` but not `18.0.0`. This is to maintain backwards compatibility when building applications that depend on specific versions. [Read more about it here](https://docs.npmjs.com/about-semantic-versioning)

An aditional note from the Now Experience docs on the [Developer Site](https://developer.servicenow.com/dev.do#!/guide/orlando/now-experience/cli/development-flow/) has the following to say about updating:

*Package managers such as npm may inadvertently hold on to outdated versions of dependencies. If after updating a dependency (or devDependency) version, you discover that your project is still referencing an older version of the dependency, follow these steps:*
```
* From the root of your repo,
  * delete the node_modules directory
  * delete package-lock.json
* Then run
  * `npm install`
```

So if you do find yourself in a dependency-nightmare, just reboot and try again! [Simple!](https://youtu.be/M0mXUC0cUPg?t=27)

That about covers updating. If you are still interested and want to know anything else, Google is your friend! If you have problems, chances are someone else has had a similar problem. 

As always, thanks!

`- Andrew`