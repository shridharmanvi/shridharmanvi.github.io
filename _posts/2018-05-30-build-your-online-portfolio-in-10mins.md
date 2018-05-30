---
layout: post
title: How to build your online portfolio in 5 mins
excerpt: "One of the first and foremost thing every software developer should do is create an online portfolio. If you cannot sell your skills, they are as good as void. In this post, I will walk you through the process of how you can to build and deploy your weibsite in 5 mins."
categories: [build-website, "101"]
comments: true
image:
  feature: https://i.imgur.com/19z94Kg.png
---
This is my first blog post on my own blog about how I built my website in less than 5 mins. I am so impressed and excited about how easy it is to do so. So let's get started...

One of the first and foremost thing every software developer should do is create an online portfolio. A place where you can showcase your skills and achievements to the world! One very easy way to do that is by using [Jekyll](https://jekyllrb.com/) to build a static website and host it on [github pages](https://pages.github.com/) (because it is free and easy to use). 

##### Before we begin, let us look at a couple of terms for better clarity:
* **static website** - A static website is a just a bunch of basic html pages. There is no interaction with a database hence making them fast and less prone to attacks. They are the most basic form of a website.
* **hosting a website** - Once your html pages are ready, they need to be hosted on a server and be accessible through the world wide web by the public. 
* **online portfolio** - A place where you can showcase your skills and easily share it with someone else via a url

##### We will be using the following to build our website:
* **git** - git is a version control system and [github](https://github.com/) is a git service with a nice UI with various features that makes development much easier for teams and individuals.
* **Jekyll** - We can either create basic html pages ourselves or have a tool do it for us - which is what jekyll does in addition to giving us the option to use additional features to make it easier to build static websites. Feel free to read more about [jekyll](https://jekyllrb.com/) as they do an awesome job of explaining what jekyll is all about.
* **github pages** - [Github pages](https://pages.github.com/) is a place where you can host your static website for free! And the way to do it is as easy as creating a repository.

If any of the above does not make sense to you, do not worry. Just follow on and I am sure things will be much clear soon...

### Pre-requesits:
1. Install ruby 
```bash
# You can use brew to install ruby on your MAC
brew install ruby
ruby -v
# You should something like below
ruby 2.3.3p222 (2016-11-21 revision 56859) [universal.x86_64-darwin17]
```
2. Next, we will install jekyll and bundler. Bundler helps us manage plugins and themes
```bash
gem install bundler jekyll
``` 
3. Install git
```bash
# MacOS comes with git, if you do not find an installation you can use the below to install
brew install git
```

Okay, now that we are all set with the pre-requesits, lets get started with building our site: 

There are two ways of doing this:
1. Build a new jekyll site from scratch and use the default theme
2. Browse github for a theme you like and just clone the repo to make it yours 

Let's do both, because - why not?

#### Build on default jekyll theme:
We can build the site from scratch and use the default theme with just a couple of commands.
```bash
# Create a new jekyll project - this will create a basic layout for you to work on
jekyll new my-site

# Navigate to my-site directory
cd my-site

# Run the server - It starts up on port 4000 by default
jekyll serve

# Now navigate to http://127.0.0.1:4000/ and you will see your site running there -- HOW COOL IS THIS?
```

#### Fork a theme:
We can fork/clone someone else's theme and change the content/config. This is what I did for the blog that you are currently reading. I cloned [leonids amazing theme](https://github.com/renyuanz/leonids/) and changed the config to mine. You can find many themes [here](https://drjekyllthemes.github.io/top) or [here](http://themes.jekyllrc.org/) and chose whichever you like.
 Once you finish cloning the repo, you can edit the `_config.yml` file to change the config for your site. Details such as site name, usernames of your social websites etc. can be listed here


#### Change the config:

```yaml
#
###################################
# Site Owner configuration
####################################
#
owner:
  name: Your Name
  job: "BARISTA"
  bio: "COFFEE IS AWESOME"
  email: #your-email
  disqus-shortname: #username
  twitter: #username
  facebook: #username
  google:
    analytics: # analytics-ID
  github: #username
  stackoverflow: #123456/username   from a "http://stackoverflow.com/users/123456/username" link
  linkedin: #username
  skype: #username
  xing: #username
  instagram: #username
```

`jekyll serve # run this command to see your new website in action locally`

#### Publishing the site to github pages:

One awesome thing about github pages is that it supports websites built with jekyll. One and only one rule that you need to follow is to name your repo in this format `username.github.io` and done. So let us do exactly that to see our website in action. If you have cloned the repo you can change its name in the settings section of the repo like this

![Change repo name](https://i.imgur.com/Kpu5qSb.png)

If you have cloned the repo, you can push it to a new repository using the following commands:
```bash
# Rename your project name:
mv old_name ./username.github.io

cd username.github.io

# Stage your changes
git add .
git commit -m 'Your changes'

# add remote
git remote add origin remote # repository URL

# verify remote
git remote -v

# Push changes
git push origin master
```

Once you push your code to the new repo (or rename the cloned repo), you should be able to see your website at the url `username.github.io`. 


***Wasn't that easy?***

Please leave your comments below if you have questions. This is my first blog and I plan on doing more of these in the future. So your comments will be greatly valuable and appreciated. 
