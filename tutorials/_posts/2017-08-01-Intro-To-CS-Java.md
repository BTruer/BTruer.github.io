---
layout: post
title:  "Installing Java; Understanding JDK, JRE, JVM, PATH, CLASSPATH, JAVA_HOME and JRE_HOME"
date:   2017-08-01 01:00:00
categories: java path classpath javahome jrehome jre jdk jvm install intro to computer science language
mytype: tutorials
---
The purpose of this article is to inform you how to install java, how to run your first java program, and to understand what happens when you run a java program.

## What is JVM, JRE, JDK?

### JVM - Java Virtual Machine
* The JVM abstracts the hardware properties so a java program can run on any platform
* It's the VM that your code runs on at run time
* Java follows the write once run anywhere principle because of the JVM.
![alt text](images/post_intro_java_1.png "JVM")
Also true for mobile devices or really any kind of device.
&nbsp;
At a high level the JVM includes
* Just in Time compiler (JIT)
* Class loader
* Java Bytecode instructions

### JRE - Java Runtime Environment
* Contains set of libraries + other files that JVM uses at runtime
* Is necessary to run java programs
* Supports commands like `java`, `javaw`, rt.jar, libraries (Math, IO, etc.)
* Contains the JVM

### JDK - Java Development Kit
* Contains development tools for java
* When installing java on your machine you usually want this one
* Supports commands like `javac`, `javap`, jars
* Contains the JRE

In short JDK contains JRE which contains JVM.

![alt text](images/post_intro_java_3.jpg "Java")
* src:http://www.oracle.com/ocom/groups/public/@otn/documents/digitalasset/2167990.jpg

![alt text](images/post_intro_java_4.png "Java")
* src:https://i.stack.imgur.comAaveN.png

## Install Java
Well first check if you have it installed already. Open up terminal or powershell/cmd.
Run the command `java -version`. If you have it installed then it should look something like this:
![alt text](images/post_intro_java_2.png "java -version")
If it is not installed it should look something like this:
![alt text](images/post_intro_java_6.png "java -version")

If you are on windows or mac you can install the jdk (java + development tools) from [here](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

You can also install it from the command line for macs and linux: `sudo packageManagerName install oracle-java`. For example ```sudo app-get install java```

You should be able to run `java` and `javac` from the command line by this point.

## What exactly happens when you run a program? What is PATH, JAVA_HOME, JRE_HOME, and CLASSPATH?
Let's see an example
1. open up a text editor and save this java program. Name it ~ HelloWorld.java ~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ java
HelloWorld.java
public class HelloWorld {
    public static void main(String[] args) {
        // Prints "Hello, World" to the terminal window.
        System.out.println("Hello, World");
    }
}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

2. Open up a terminal and moved to where you save HelloWorld.java `cd location/subdir`
3. Compile and then run the program `javac HelloWorld.java` and `java HelloWorld` ![alt text](images/post_intro_java_7.png "java")

So what exactly is going on when you type the command `java` and `javac`. Where is this running from? For this we need to understand what environmental variables are.

*Environment Variables* are global variables that are accessible by all the processes running on the OS.
*PATH* is an environmental variable that maintains a list of directories for executable programs like `java`, `javac`, `ls`, `cd`, etc.
*CLASSPATH* is an environmental variable that maintains a list of directories for java class files or jars.
*JAVA_HOME* is an environmental variable that maintains the location of the installed JDK.
*JRE_HOME* is an environmental variable that maintains the location of the installed JRE.


LINKS/SOURCES:
1. http://www3.ntu.edu.sg/home/ehchua/programming/howto/environment_variables.html
2. https://www.javatpoint.com/difference-between-jdk-jre-and-jvm
3. http://www.journaldev.com/546/difference-jdk-vs-jre-vs-jvm
4.  https://stackoverflow.com/questions/1906445/what-is-the-difference-between-jdk-and-jre
