---
layout: post
title:  "From Nothing to Something - How to Build a Static Website with Github and Jekyll"
tags: how to, create, website, github, jekyll, blog, post, pages, linux, windows, osx, tutorial
---
"Hello world" - is how you start your CS/programing education (usually). So this post will explain in detail how to get a baseline website like this:

#Step 1 - Set up the environment
Have a OSX or Linux machine. Why? Bash. And when searching for help and tutorials online it is assumed your environment will be working with Bash not DOS(PowerShell). Cywin is not a good replacement. In general, web development is simpler to do on Linux and OSX, unless you are working with .NET of course. Although with bash support for Windows10 around the corner it's tough to say but I will post about it once it's officially released. If you are going from WIN10/8.1/7 to Linux for the first time [Ubuntu](http://www.ubuntu.com/download/desktop) is a good option. If you are familiar with the linux file system or just want a lightweight OS [Debian](https://www.debian.org/CD/live/) is a great choice (with gui unless your a terminal pro). Create a [USB booter](http://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/) after downloading the ISO and install the OS.

Bottom line - make sure you have a good development environment with minimal distractions, files, and programs.

#Step 2 - Git and Github
1. Go to (Github.com)[http://github.com]
2. Create an account
3. Create a new repository called: username.github.io     where username is your github name
4. Open up terminal(PowerShell if WIN10) and know your [systems package manager](http://distrowatch.com/dwres.php?resource=package-management)
5. Run ```sudo apt-get install update``` to make sure your package manager is up to date. Replace ```apt-get``` with your package-manager. Run ```sudo apt-get install git```. If you are using (WIN10 or OSX)[https://git-scm.com/book/en/v2/Getting-Started-Installing-Git] just download and install as usual.
6. Now just check if it is properly installed by just typing ```git``` and you should see
>usage: git [--version] [--help] [-C <path>] [-c name=value]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]
start a working area (see also: git help tutorial)
   clone      Clone a repository into a new directory
   init       Create an empty Git repository or reinitialize an existing one
work on the current change (see also: git help everyday)
   add        Add file contents to the index
   mv         Move or rename a file, a directory, or a symlink
   reset      Reset current HEAD to the specified state
   rm         Remove files from the working tree and from the index
examine the history and state (see also: git help revisions)
   bisect     Find by binary search the change that introduced a bug
   grep       Print lines matching a pattern
   log        Show commit logs
   show       Show various types of objects
   status     Show the working tree status
grow, mark and tweak your common history
   branch     List, create, or delete branches
   checkout   Switch branches or restore working tree files
   commit     Record changes to the repository
   diff       Show changes between commits, commit and working tree, etc
   merge      Join two or more development histories together
   rebase     Forward-port local commits to the updated upstream head
   tag        Create, list, delete or verify a tag object signed with GPG
collaborate (see also: git help workflows)
   fetch      Download objects and refs from another repository
   pull       Fetch from and integrate with another repository or a local branch
   push       Update remote refs along with associated objects
'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.

7. Now in the terminal move into a location that you want to put your code into ex: ```cd Documents/this/is/where/i/put/my/code/```
8. Before we continue it is important to ```git config user.name yourGithubUserNameHere```.```git config user.email yourEmailForGithubHere```. Now just test it before you continue. So ```git config user.name``` and ```git config user.email``` and you should see whatever you just set.
9. Now we need the repository which on github onto our local machine. So ```git clone https://github.com/username/username.github.io.git``` where username is your username for github.
10. Move into the new folder that appeared ```cd username.github.io```

#Step 3 - Ruby and Jekyll
1. Get the Ruby development package ```sudo apt-get install ruby-dev```
2. ```sudo apt-get install ruby```. Now when you type ```gem``` and ```ruby --version``` you should not get any errors.
3. ```gem install jekyll``` - add sudo if it doesn't work because of permission reasons. Check that it is installed correctly with ```jekyll --version```
4. Now double check your terminals current directory with ```pwd``` and you should see something like "/home/user/Documents/whereeverYouPutCode/username.github.io"
5. Now that you are in the right spot run and the folder you are in is empty (remove the README.md temporarily and put it back in later) ```jekyll new .```

#Step 4 - Push the repository to github
1. Assuming you are still in the repository folder of which you just created the jekyll site with the following files/folders: ```_config.yml _layouts    _sass   css     index.html
_includes   _posts      about.md    feed.xml README.md(added back in)```, run ```git status``` and you should see some red text. These are unattached and uncommitted files and changes.
2. Run ```git add .``` This command added all the unattached files to the repository.
3. Run ```git commit -m "your message here or First commit with jekyll site"```
4. Run ```git push origin master``` and you will need to put in your account information

#Step 5 - Rejoice for a Moment
1. Go to your favorite browser and in the address type in ```username.github.io``` - that's your site!
2. Now begin making it your own... i'll save that for another tutorial.

Note in general it is best practice to ```jekyll build``` which will generate a "\_site" folder

Helpful links/tutorials:
  Jekyll build watch serve ***important read***: http://jekyllrb.com/docs/usage/
  Markdown syntax for blog post that go in ```_posts``` https://guides.github.com/features/mastering-markdown/   https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#blockquotes
  ZacBlanco's tutorial: http://blanco.io/blog/jekyll/building-a-site-with-jekyll
