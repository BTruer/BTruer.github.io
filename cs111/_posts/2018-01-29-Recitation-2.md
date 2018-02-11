---
layout: post
title: "Recitation 2: Variables, Initialization, Assignment, Declaration, Boolean Expressions, installing and running java programs"
date: 2018-01-29 01:00:00
categories: intro computer science recitation installing java
mytype: cs111
---

# Recitation 2 What are variables? What is declaration, assignment, initialization, a boolean expression, types, and syntax?

A variable is a piece of memory that can contain a data value.

A declaration is writing out the type and variable name. `<type> <var name>;` ex. `int x;`

An initialization is assigning a value to a variable `<var name> = <value>;` ex. `x = 5;`

An assignment is the whole thing, meaning you do both. `<type> <varname> = <value>;` ex. `int x = 5;`

In programming languages every variable has a type. In java there are two categories: primitives and reference. Let's focus on primitives for now. They are:

** int  -- ex. 1,5,-800
** float -- ex. 5.0
** double -- ex. 6.0
** char -- ex. 'a','@','!','Z'
** boolean -- ex. true, false

Boolean expressions evaluate to true or false. They use operators like `<`,`<=`,`&&`,`||`,`!`. You can find these expressions in the conditional part of if statements. Boolean expression can be found in the parenthesis of `if(<Boolean Expression>)`, `while(<Boolean Expression>)`, and `for(;<Boolean Expression>;)`. 

# How to install Java, compile and run java code
The extended post is [here](http://bhargavtarpara.com/Installing-Java-Understanding-JDK-JRE-JVM-JAVA_HOME), which describes what exactly the JDK and all of this is, but here are the steps and basics.

1.1. Download the [JDK (java so you can code in it and run your programs)](http://www.oracle.com/technetwork/java/javase/downloads/jdk9-downloads-3848520.html) for your operating system.

2.2. Run the installer (whatever.EXE for windows, something.dmg for OSX, or run a command this command for linux `sudo dpkg -i /path/to/deb/file followed by sudo apt-get install -f` )

3.3. Open up CMD/Powershell (windows) or Terminal (OSX, Linux)

4.4. Type in the command `java` and you should see a bunch of text. `java -version` will also let you know if you have it installed and will obviously output the version.

5.5. Type in the command `javac` and you should see some documentation like `Usage: javac <options> <source files>                                     where possible options include:`. Now if you are on windows and don't see it you should update your system path variable to include the bin folder. [Here](https://stackoverflow.com/questions/32241179/setting-up-enviromental-variables-in-windows-10-to-use-java-and-javac) is a [link](https://javatutorial.net/set-java-home-windows-10) or too on how to do that. If you have a MAC [here](http://www.sajeconsultants.com/how-to-set-java_home-on-mac-os-x/) is how to set the path variable.

6.6. Now the commands you need to know are `cd <folder/path>` (`cd ..` to go up a directory), `pwd` (tells you where you are in your file system), `javac <FileName.java>` - to compile, `java <FileName>` - to run. Technically your filename is the same as your class name as we will learn later in the semester. 