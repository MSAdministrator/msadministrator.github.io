---
layout: post
title: "Setting up GitHub Pages and reveal.js presentations"
date: 2017-09-04
excerpt: "With GitHub pages and reveal.js you can create amazing websites and presentations"
tags: [revealjs, presentations, websites, github]
comments: true
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
