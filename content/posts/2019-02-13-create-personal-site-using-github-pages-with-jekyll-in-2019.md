+++ 
draft = false
date = 2019-09-20T04:55:16-04:00
title = "Create personal site using Github Pages with Jekyll in 2019"
description = "A simple way to start personal blogging, using Jekyll and GitHub Pages."
slug = "" 
tags = ["jekyll","github pages"]
categories = ["static site"]
externalLink = ""
series = []
+++

![Don't be shy](https://i.imgur.com/SlmRvNI.png)

This tutorial uses `User and Organization Pages` for general usage personal site

## Create github pages repo
Follow instructions from [GitHub Pages][GitHub Pages], to create a user site repo (Remember to initialize it with a `README.md` file). Here we use my own repo [foodtooth.github.io][foodtooth.github.io] for simplicity.

## Generate default jekyll site
1. Install Jekyll. Refer to [jekyll installation doc][jekyll installation doc]
2. 
```bash
git clone https://github.com/foodtooth/foodtooth.github.io
jekyll new --force foodtooth.github.io
cd foodtooth.github.io
```
3. Follow instructions in `Gemfile` to enable `gem "github-pages"`
4. `bundle update`
5. Copy the content of [this gitignore][this gitignore] to `.gitignore` file
6. `bundle exec jekyll serve` to start jekyll on local

Now, you are running a default jekyll site on local. Feel free to do the editing and push the repo to github when you are ready.

## Further instructions
If you hesitate about choosing the right theme to use, pick [minimal-mistakes][minimal-mistakes github]. Beautiful and simple looking, detailed and nice [documentation][minimal-mistakes docs]. After walking through the documentation and doing some editings, your personal blog is good to go.

![Show off](https://i.imgur.com/faQfm3L.jpg)

[GitHub Pages]: https://pages.github.com/
[foodtooth.github.io]: https://github.com/foodtooth/foodtooth.github.io
[jekyll installation doc]: https://jekyllrb.com/docs/installation
[this gitignore]: https://www.gitignore.io/api/vim,git,linux,jekyll,eclipse,sublimetext
[minimal-mistakes github]: https://github.com/mmistakes/minimal-mistakes
[minimal-mistakes docs]: https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/