---
layout: post
title:  "From Nothing to Something - How to Build a Static Website with Github and Jekyll"
tags: how to, create, website, github, jekyll, blog, post, pages, linux, windows, osx, tutorial
---
"Hello world" - is how you start your CS/programing education (usually). So this post will explain in detail how to get a baseline website like this:

# Step 1 - Set up the environment
Have a OSX or Linux machine. Why? Bash. And when searching for help and tutorials online it is assumed your environment will be working with Bash not DOS(PowerShell). Cygwin is not a good replacement. In general, web development is easier to do on Linux and OSX, unless you are working with .NET of course. Although with bash support for Windows10 around the corner it's tough to say but I will post about it once it's officially released. If you are going from WIN10/8.1/7 to Linux for the first time [Ubuntu](http://www.ubuntu.com/download/desktop) is a good option. If you are familiar with the linux file system or just want a lightweight OS [Debian](https://www.debian.org/CD/live/) is a great choice (with gui unless your a terminal pro). Create a [USB booter](http://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/) after downloading the ISO and install the OS.

Bottom line - make sure you have a good development environment with minimal distractions, files, and programs.

# Step 2 - Git and Github
1. Go to [Github.com](http://github.com)
2. Create an account
3. Create a new repository called: username.github.io where username is your github name
4. Open up terminal (PowerShell if WIN10) and know your [systems package manager](http://distrowatch.com/dwres.php?resource=package-management)
5. Run ```sudo apt-get install update``` to make sure your package manager is up to date. Replace ```apt-get``` with your package-manager. Run ```sudo apt-get install git```. If you are using [WIN10 or OSX](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) just download and install as usual.
6. Now just check if it is properly installed by just typing ```git --version``` and you should see 2.something (or maybe 3 if that is released when you are reading this).
7. Now in the terminal move into a location that you want to put your code into ex: ```cd Documents/this/is/where/i/put/my/code/```
8. Before we continue it is important to ```git config user.name yourGithubUserNameHere```, ```git config user.email yourEmailForGithubHere```. Now just test it before you continue. So ```git config user.name``` and ```git config user.email``` and you should see whatever you just set.
9. Now we need the repository which on github onto our local machine. So ```git clone https://github.com/username/username.github.io.git``` where username is your username for github.
10. Move into the new folder that appeared ```cd username.github.io```

# Step 3 - Ruby and Jekyll
1. Get the Ruby development package ```sudo apt-get install ruby-dev```
2. ```sudo apt-get install ruby```. Now when you type ```gem --version``` and ```ruby --version``` you should not get any errors.
3. ```gem install jekyll``` - add sudo if it doesn't work because of permission reasons. Check that it is installed correctly with ```jekyll --version```
4. Now double check your terminals current directory with ```pwd``` and you should see something like "/home/user/Documents/whereeverYouPutCode/username.github.io"
5. Now that you are in the right spot run and the folder you are in is empty (remove the README.md temporarily and put it back in later) ```jekyll new .```

# Step 4 - Push the repository to github
1. Assuming you are still in the repository folder of which you just created the jekyll site with the following files/folders: ```_config.yml _layouts    _sass   css     index.html
_includes   _posts      about.md    feed.xml README.md(added back in)```, run ```git status``` and you should see some red text. These are unattached and uncommitted files and changes.
2. Run ```git add .``` This command added all the unattached files to the repository.
3. Run ```git commit -m "your message here or First commit with jekyll site"```
4. Run ```git push origin master``` and you will need to put in your account information

***Note*** in general it is best practice to ```jekyll build``` which will generate a "\_site" folder (locally - you dont need on repo) and ```jekyll serve``` to check what the site will look like at localhost:4000

# Step 5 - Rejoice for a Moment
1. Go to your favorite browser and in the address type in ```username.github.io``` - that's your site!
2. Now begin making it your own... i'll save that for another tutorial.



## _Helpful links/tutorials:_

  1. Jekyll build watch serve ***important read***: [http://jekyllrb.com/docs/usage/](http://jekyllrb.com/docs/usage/)
  2. Markdown syntax for blog post that go in ```_posts``` [https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)   [https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#blockquotes](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#blockquotes)
  3. [ZacBlanco's tutorial](http://blanco.io/blog/jekyll/building-a-site-with-jekyll)
