---
layout: post
title:  "Using Jekyll and Github pages for a blog site"
date:   2019-07-17 15:15:00 +0100
categories: how-to
---

## Intro

I've just set up this blog so I can relay information and instructions on how to set up applications and environments related to DevOps and System Administration. I'm hoping this will be useful for other people but that it may also be useful for helping me to get used to blogging frequently and to have a single place to store the information I learn on a day-to-day basis.

So I thought I'd get started with how I set up this blog.

I went with Jekyll and Github pages predominently because it seemed simple to manage. I didn't want to have to worry about databases, configuration and the like. I've used Wordpress previously and well, if you don't update that thing frequently it quickly becomes vulnerable to just about everything.
I liked the idea of using markdown and as the site would be stored on Github anyway so using Github pages was a simple way to host the site.

## Installing Jekyll

I'm using WSL for my local environment but any Linux machine will work.

Install the full Ruby development environment:

```bash
sudo apt-get install ruby-full build-essential zlib1g-dev
```

Set up a Gem installation directory for your user account:

```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

Install Jekyll:

```bash
gem install jekyll bundler
```

The simpliest and easiest way to get started is to use the default Jekyll site. You can do this by creating a new site:

```bash
jekyll new <site_name>
```

You can then `cd` into the folder created by that command and run `jekyll serve` to start a webserver to access your site on `http://localhost:4000`.

There's a very useful step-by-step demo on the Jekyll site that will help you understand how it works and goes into a lot more detail than I have here.

You can edit the index or about pages by editing the markdown files in the site folder, add a post in the `_posts` folder and edit some of the other site content by editing the variables in the _config.yml file.

At the moment the site is configured with a minimilist basic theme called Minima but you can use other themes which you will need to install by editing the Gemfile and adding it. You can also edit the css yourself but that requires some changes that I won't go into here.

## Running the site on Github pages

