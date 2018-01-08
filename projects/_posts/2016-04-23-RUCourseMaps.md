---
layout: post
title: "RUCourseMaps"
date: 2016-04-23 01:00:00
categories: python flask application
mytype: projects
---

### When
HackRU Spring 2016

### Who
Roopesh K, Alex Jia, and I

### What
An application that lets students plan out which courses to take by displaying a dependency tree of
courses by prereq using Python, HTML/CSS + Bootstrap and Heroku

### Process
* * Take course data from `http://sis.rutgers.edu/soc/courses.json?...` and parse for courses and prereq.
* * Take this list and sends it to the frontend where it is each item in the list is actually a key value pair `{course : prereq}`. Then using cytoscape a graph is dynamically generated.

### Results
Won best Rutgers Hack

![alt text](images/post_rucm.jpg)
