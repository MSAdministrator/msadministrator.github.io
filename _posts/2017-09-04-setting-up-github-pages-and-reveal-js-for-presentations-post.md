---
layout: post
title: "Setting up GitHub Pages and reveal.js presentations"
date: 2017-09-04
excerpt: "With GitHub pages and reveal.js you can create amazing websites and presentations"
tags: [revealjs, presentations, websites, github]
comments: false
---

Using GitHub Pages and reveal.js you can create amazing websites, and portable presentations that are beautiful.  To get started creating amazing presentations and a website using GitHub Pages you will need the following:

* GitHub account
* Reveal.js - https://github.com/hakimel/reveal.js/

To utlitize both successfully, I am going to create a main webpage using GitHub Pages. Additionally, I am going create a second "website" that will host all of my presentations (these are purposely seperated for clear segmentation reasons).  I suggest you do the same.

Okay, here we go.  I want to say, if you run into any issues while following this post please leave a comment and let me know!

1. Assuming you have a GitHub account already, you first need to create 2 new repositories.  The first will be your root page, and this will contain your landing page of sorts.  The second will be where you will host your presentations.
    1. Create a new repository with the name of {username}.github.io.  In my case, my repositories name would be msadministrator.github.io.  You can find what you should be naming your repository by logging into GitHub and going to your profile.  The URL should be "https://github.com/{username}.
    2. Create a second new repository with the name of either 'presentations' or 'slides' (it's up to you).
2. The second step is that we will need to either set a theme in our GitHub repository settings or we will need to get a new theme.  I'm going to show you how to find a theme and download it.
    1. Go to http://jekyllthemes.org/ and find a theme that you like in the list.  Once you have one, then go to that themes page and select the theme's "Homepage" button and fork the repository or just download/clone it to your local machine.  Either way, we need this on our machine.  I have choosen to go with the Moon theme (http://jekyllthemes.org/themes/moon/)
    2. Once you have the theme downloaded, you need to edit the _config.yml with your information.  Go do that, i'll wait.
    3. Removing any sample posts from the _posts folder and add your own (i'm doing this part as I'm writing this post)
    4. Edit the `index.md` file in the `about` folder
    5. Once you have done all this, you need to push this (downloaded theme code) to your new repository.  Again, in my case this would be `msadministrator.github.io`
3. Do a git clone to your local machine by running `git clone git@github.com:username/username.github.io.git` 
4. You should now have a copy of your empty repository named `username.github.io` on your local machine
4. Add/copy the files from your downloaded template (earlier, mine was the Moon template) to this new empty folder on your machine named `username.github.io`.
5. Once in your `username.github.io` folder on your machine (via terminal), then you need to run `git add .`
6. Next, we will run the following command `git commit -m 'Adding new root files to GitHub pages repository'`
7. Next, we run `git push origin`

You should now be able to go (after a few minutes) to your customized URL.  This should be accessible by navigating to `username.github.io` in your web browser.  For instance, mine is `msadministrator.github.io`

## Some Gotchas
So, once you push your code to your `username.github.io` master branch, it should build successfully.  But, if it doesn't you may have some issues with your `_config.yml` file.  So, I recommend you use the following linter to verify that your yaml file is correct: https://codebeautify.org/yaml-validator.  I had an issue with using an apostrophe in my `description` key: value pair.


# Creating and Display awesome Presentations
Okay, for this one we can approach this a couple of different ways.  The first way involves downloading https://github.com/hakimel/reveal.js/ from GitHub and building my pages manually.  This works, but there's a lot of syntax that you may not want to get into.  If you do, then great!  This is the way, and you can just follow that repo's instructions. Done

If you want to know, in my opinion, an easy/quicker way then please continue reading.

The first step is to make sure you have created a new repository in GitHub named (up to you) either `presentations` or `slides` or something.  Once you have done that, then follow these steps:

1. The first thing you need to do is to run `git clone git@github.com:username/presentations.git` to clone your empty repository to your local machine
2. Next, let's cd into our repository folder on our local machine
3. Run the following to create a new `orphaned` branch: `git checkout -b gh-pages --orphan`
4. If you run `git branch` you should see that you are now on a new branch named `gh-pages`
5. Next, you can clone the `reveal.js` repository mentioned above or you can do what I did and went to https://slides.com/ 
    1. Basically, https://slides.com/ is a GUI editor that will do the same thing as writing and manipulating the reveal.js code, but visually.  It's much faster to get use to, so you can sign up for a new account and begin creating your presentation.  
    2. Once complete, then you can export your newly created presentation.
6. Once you have either an export from slides.com or a customized page using reveal.js source files, then you need to drop them into your `presentations` or `slides` folder.  You can create a sub-folder in your `presentations` folder with the name of the presentation as the folder name, but I only did this for specific images.
    1. To make this easier on you, I would just suggest that you clone my repository here and modify as needed: https://github.com/MSAdministrator/presentations/tree/gh-pages
7. Once you have done that, then you can reference it via a link on your `username.github.io` site or access it directly by going to `username.github.io/presentations`

# Recap
We have now created a few things here that are useful.  The first being our new repsitory named `username.github.io` and we have added a theme to the `master` branch on this repository.  

Next we have created another repository named `presentations` or `slides` and it includes it's own landing page (if you cloned my repo).  Here is the full path for my example: `msadministrator.github.io/presentations`

Since we have added our exported slides.com presentation to a sub-folder within our `presentations` repository, you can now access this presentation directly by going to `https://msadministrator.github.io/presentations/basics-of-incident-handling.html`.

### Layout

1. My Accounts Root (https://github.com/MSAdministrator)
    1. GitHub Pages Root (https://msadministrator.github.io/) - Full Path (https://github.com/MSAdministrator/msadministrator.github.io)
    2. Presentations Root (https://msadministrator.github.io/presentations/) - Full Path (https://github.com/MSAdministrator/presentations/tree/gh-pages)
        1. Basics of Incident Handling Presenation (https://msadministrator.github.io/presentations/basics-of-incident-handling.html#/)