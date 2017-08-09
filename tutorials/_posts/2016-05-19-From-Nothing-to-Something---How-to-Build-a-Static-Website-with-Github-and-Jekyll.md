---
layout: post
title:  "From Nothing to Something - How to Build a Static Website with Github and Jekyll from Scratch or Jekyll themes"
date:   2016-05-10 01:00:00
categories: how-to create website Github jekyll blog post ghpages 2017
mytype: tutorials
comments: true
---
"Hello World" - is how you start your CS education. So this post will explain in detail how to get a baseline personal website like this. There are two ways: you can use Github's default style or just download a template and drag it into the repo.

# Step 1 - Set up the environment
Have Bash (commandline interface). If you are Linux or OSX your good. If you have Windows install it. Here is a tutorial for that.

# Step 2 - Git and Github
1. Go to [Github.com](http://github.com)
2. Create an account
3. Create a new repository called: username.github.io where username is your github name
4. Open up terminal (PowerShell then ```bash``` if Windows) and know your [systems package manager](http://distrowatch.com/dwres.php?resource=package-management)
5. Run ```sudo apt-get install update``` to make sure your package manager is up to date. Replace ```apt-get``` with your package-manager. Run ```sudo apt-get install git```. If you are using [WIN10 or OSX](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) just download and install as usual.
6. Now just check if it is properly installed by just typing ```git --version``` and you should see 2.something (or maybe 3 if that is released when you are reading this).
7. Now in the terminal move into a location that you want to put your code into ex: ```cd this/is/where/i/put/my/code/```
8. Before we continue it is important to ```git config --global user.name yourGithubUserNameHere```, ```git config --global user.email yourEmailForGithubHere```. Now just test it before you continue. So ```git config user.name``` and ```git config user.email``` and you should see whatever you just set.
9. Now we need the repository which on github onto our local machine. So ```git clone https://github.com/username/username.github.io.git``` where username is your username for github.
10. Move into the new folder that appeared ```cd username.github.io```

# Step 3 - Ruby and Jekyll
1. Get the Ruby development package ```sudo apt-get install ruby-dev```
2. ```sudo apt-get install ruby```. Now when you type ```gem --version``` and ```ruby --version``` you should not get any errors.
3. ```gem install jekyll``` - add sudo if it doesn't work because of permission reasons. Check that it is installed correctly with ```jekyll --version```
4. Now double check your terminals current directory with ```pwd``` and you should see something like "/whereeverYouPutCode/username.github.io"
5. Now that you are in the right spot run and the folder you are in is empty (remove the README.md temporarily and put it back in later) ```jekyll new .```

# Step 4 - Push the repository to github
1. Assuming you are still in the repository folder of which you just created the jekyll site with the following files/folders: ```_config.yml _layouts    _sass   css     index.html
_includes   _posts      about.md    feed.xml```, run ```git status``` and you should see some red text. These are unattached and uncommitted files and changes.
2. Run ```git add --a``` This command added all the unattached files to the repository.
3. Run ```git commit -m "your message here or first commit"```
4. Run ```git push origin master``` and you will need to put in your account information

***Note*** To develop your site locally without putting the changes out onto your actual site just go ```jekyll serve```. This will create an ```_site``` folder which you should add to your gitignore.

# Step 5 - Rejoice for a Moment
1. Go to your favorite browser and in the address type in ```username.github.io``` - that's your site!
2. Now begin making it your own. Understand the file structure of Jekyll.

# Step 4 - Alternative way to customize the look
1. Go to [jekyll themes](https://www.google.com/search?q=jekyll+themes) and find a theme you like.
2. Download the zip or even clone the repo either is fine.
3. Copy and paste the contents of the theme into your empty username.github.io directory


# Helpful links/tutorials:
1. Jekyll file structure ***important read***: [http://jekyllrb.com/docs/usage/](http://jekyllrb.com/docs/usage/)
2. Markdown syntax for blog post that go in ```_posts``` [https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)   [https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#blockquotes](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#blockquotes)
3. [ZacBlanco's tutorial](http://blanco.io/blog/jekyll/building-a-site-with-jekyll)
