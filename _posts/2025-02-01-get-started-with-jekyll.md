---
layout: post
title: Getting Started with Jekyll
description: Get started with Jekyll basics in this comprehensive overview. You will learn how to install and configure, as well as deploy it to a web server.
date: 2025-02-01 11:20 +0700
categories: [Jekyll]
tags: [getting started]
author: khang
---


## My First Steps into Blogging
Blogging has always fascinated me, but I never knew where to start. After exploring different options, I stumbled upon [**Jekyll**](https://jekyllrb.com/) - a simple, powerful static site generator that makes writing and publishing blogs a breeze.

This blog marks my first step into the world of blogging, and I want to share my journey with you. Whether you are a developer looking for a lightweight blogging platform or a beginner like me, this guide will walk you through setting up [**Jekyll**](https://jekyllrb.com/), creating your first post, and getting your blog online. Let's dive in!

## Why Jekyll?

✅ Fast & Lightweight – Jekyll generates static HTML, making it faster than [WordPress](https://wordpress.com/) (which relies on a database) and [Docusaurus](https://docusaurus.io/) (which uses React).

✅ Free & Easy Hosting – Can be hosted for free on GitHub Pages, unlike WordPress, which often requires paid hosting.

✅ Full Control – No platform restrictions like [Medium](https://medium.com/) or [Substack](https://substack.com/about); you own your content and customize everything.

Moreover, you just need to know how to write a markdown file for publishing a blog, and I recommend the beginners to use [stackedit](https://stackedit.io/ "markdown editor tool") or [editor md](https://pandao.github.io/editor.md/en.html).

## Installation

### Step 1. Choosing theme
In addition to default theme, you can find some Jekyll themes on public website and choose which is suitable for you:
-   [https://jekyllthemes.io/](https://jekyllthemes.io/)
-   [http://jekyllthemes.org/](http://jekyllthemes.org/)
-   [https://jekyll-themes.com/](https://jekyll-themes.com/)
-   [https://jamstackthemes.dev/ssg/jekyll/](https://jamstackthemes.dev/ssg/jekyll/)

My choice is [chirpy](https://github.com/cotes2020/chirpy-starter) as it has dark theme.

### Step 2. Activating the Github Pages
After choosing a Jekyll theme, the next step is to host it on GitHub Pages. Each theme typically includes setup instructions, however, as my observation, here are the general steps:

1. Create repository.
    - If it is a GitHub template, click the <kbd>Use this template</kbd> button beside  <kbd>Star</kbd> button, and then
    select <kbd>Create a new repository</kbd>.
    - Else, <kbd>Fork</kbd> the theme repository.

2. Name the new repository  `<username>.github.io`, replacing  `username`  with your lowercase GitHub username.

> (Optional) Some themes require to set the `url` in `_config.yaml` to protocol & hostname (e.g. 'https://username.github.io') for your site .
{: .prompt-info }

> You should go to `Settings` &rarr; `Pages` &rarr; `Build and Development` to ensure the source is chosen as `Github Actions` or `Deploy from a branch` (you need to specify branch name).
{: .prompt-tip }

But you don’t want just a template, you want to customized it to yourself. So, let’s move on to the next step.

### Step 3. Customizing by your choice

1. Clone the repository you just created.

2. Install Ruby and Jekyll on your machine through the [official guide](https://jekyllrb.com/docs/installation/).
For Windows users:
    - Download and install Ruby from [RubyInstaller](https://rubyinstaller.org/) and follow the instructions.
    - Once your computer has Ruby, install Jekyll and Bundler using `gem install jekyll bundler`.
    - Check if Jekyll has been installed properly: `jekyll -v`

3. `cd` to your project folder and run `bundle install` to install the required gems.

4. Update the variables of `_config.yml` as needed. Some of them are typical options.
    - `title` is the the main title of your website
    - `avatar` is the profile picture in the sidebar
    - `timezone` is used to display the date and time of your posts
    - `lang` is the language of the site

5. Run `bundle exec jekyll s` to start the local server.

> Add flag `--livereload` to automatically reload the site when code changing (excepts for file `_config.yaml`).
{: .prompt-tip }

After a few seconds, the local server will be available at [http://127.0.0.1:4000](http://127.0.0.1:4000).

### Step 4. Updating change
To update your change in GitHub Pages, commit your code to repository using these command lines:

```terminal
git add .
git commit -m '<commit message>'
git push
```

## Conclusion

Now you've had your own customized site, the next part is writing blog. Stay tuned, and see you in the next part! Thanks for your reading. Please leave the comment if you have any questions or feedbacks.