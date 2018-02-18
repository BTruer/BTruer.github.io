---
layout: post
title: "Recitation 4: Java, if, else, if else"
date: 2018-02-11 01:00:00
categories: intro computer science recitation java if else elseif
mytype: cs111
---

### Java if statement

Let's first look at the anatomy of the humble `if` statement:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ java

if(<boolean expression>){
	//if boolean expression evaluates to true then execute code here
}
//if boolean expression evaluates to false OR code inside the if statement finishes then execute code here 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Note that there are other ways of writing it.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ java

if(<boolean expression>)
	//if boolean expression evaluates to true then execute code here

//if boolean expression evaluates to false OR code inside the if statement finishes then execute code here 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

### Java if else statement


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ java

if(<boolean expression>){
	//if boolean expression evaluates to true then execute code here
} else {
	//if boolean expression evaluates to false then execute code here	
}
//then execute code here 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ java

if(<boolean expression>)
	//if boolean expression evaluates to true then execute code here
else
	//if boolean expression evaluates to false then execute code here	

//then execute code here 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


### Java if elseif

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ java

if(<boolean expression 1>){
	//if boolean expression 1 evaluates to true then execute code here
} else if(<boolean expression 2>){
	//if boolean expression 2 evaluates to true then execute code here	
} else {
	//any other case the code here executes
}
//then execute code here 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Some examples are [here](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/if.html).