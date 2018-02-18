---
layout: post
title: "Recitation 3: Java type casting and java using libraries/packages"
date: 2018-02-04 01:00:00
categories: intro computer science recitation java type casting libraries
mytype: cs111
---

### Type casting primitives in Java
Let's first take a look at something familiar:

`int a = 5;`
`double b = 6.0;`

These are assignment statements that have the same type on left as on right. Now what about this:

`double b = 5;` 
Is this allowed? Is there a problem? Well the type on the left is a double and the value on the right is an int. So is this allowed - yes, it will implicitly be casted as a double. If you try to print this out you will see `5.0` not `5`.
Now what about the opposite?
`int a = 5.1;`
Is this allowed - no java will not automatically cast this. So then how do you cast (explicitly) this?
`a = (int)5.1; // a is 5`

Note that casting to an int will truncate anything so:

`a = (int)5.9999; // a is still 5`


One important note on casting it works on the variable or value directly to the right.

`int a = 5;`
`double c = 12.988;`
`int b = (int)c/a `
So now what will `b` evaluate to?
(int)12.988/5 ==> 12/5 ==> 2.4 ==> 2 (because b is an int after the devision is complete it will just keep the whole number 2)
So b is 2.


### Imports in Java and how to use the IO and Math library

In general you in java you import packages which are bunch of classes put [together](https://www.leepoint.net/language/10basics/import.html).

For now lets stick with a simple model of where you put your code, let's say your desktop. When you open up your shell you should move into the desktop where your code is. Let's say it in a folder called CS. In general when yo want to use already written code or someone else code via a library you would import the library like so:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ java
Sum.java
import java.lang.Math;
public class Sum {
    public static void main(String[] args) {
        System.out.println(Math.exp(1.0));   	// prints e^1 which is 2.718281
        int input_from_user = IO.readInt(); 	//gets an int from the user and saves it to the variable
    }
}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Here the library import is Math. This [page](http://www.mathcs.emory.edu/~cheung/Courses/170/Syllabus/04/java-lib.html) goes into the details of importing. Technically *you don't need to include the import statement because java will automatically import any java.lang.anything* 
Now let's download [IO.java](/IO.java) (a class that simplifies getting input and returning output to the user; Also streamlines our grading process via autolab).
In the code above we have not imported the library so how are we still able to use it? This is because *Sum.java is in the same directory as IO.java so we can use all of IO's methods*. The methods and class are public so other programs can access it. Therefore we can use IO.java just by putting it in the same directory. Now if you are using eclipse you have packages and you will need to have package statements for each class Sum and Math.