---
layout: post
title: "Recitation 1: 8 Coin Problem, Truth Tables, Boolean Expressions"
date: 2018-01-22 01:00:00
categories: intro computer science recitation
mytype: cs111
---

# Recitation 1
What is Computer Science? What is a programmatic way of solving something? Lets say I'm an alien and I don't know how to tie shoes. How would you describe the process of tying shoes to an alien or really a child who has no idea. You may say "Take your left hand and grab the left lace and then take your right hand and grab the right lace. Then pull them up and cross them over etc." Describing these steps is a systemic way of tying ones shoes that can be repeated. This description is what is known as an algorithm or put simply a step by step process of achieving something or computing something.

## The Coin Problem (8 coin, 9 coin, 13 coin)
Imagine you have 8 identical coins. However one of them is fake. It weighs slightly less or more then the other 7. You have a balance scale that you can use up to 3 times. The balance has two sides. If the weight of the objects on one side is equal to the weight of the objects on the other side then the balance will remain equal or level (flat) else the heavier side will drop and the other will elevate. So: given these 8 coins and a balance that you can use 3 times how would you find the bad coin?

Well what is our initial intuitive approach? Put 4 and 4 and see which side has the bad coin. Okay: you put the coins on 4 and 4 but then which side has the bad coin? We don't know if the bad coin is heavier or lighter. So we don't know which pile of 4 coins to then start looking in. In other words we have now wasted the first weigh because now we have no additional information or we have not eliminated any choices.

## Solution to the coin problem

When we think programmatically or in CS we want to break the problem down int o its most simple components. What is the most basic problem? 

Let's look at a simpler problem. When you have 3 coins and one of them is bad (lighter or heavier fake coin) and you have a scale that you can use 2 times. If you put two coins on the balance there are two possible results. The coins balance (equal) or they are unequal. If the coins balance then we know that the bad coin is the third one that is not on the balance. If the balance is unequal we can take one off and put the third one on. If the coins are equal in weight the bad coin is the one we took off else it is the one was in both weighs.

![8 coins](images/coinproblem.jpg "Coin problem")

We can now extend this logic to 8 coins (A,B,C,D,E,F,G)
1st weigh:	AB vs CD  and EFGH is off to the side
if balanced we know the bad coin is in EFGH
else we know the bad coin is in ABCD

Now we have 4 coins and two weighs either way (ABCD or EFGH)

2nd weigh: A vs B OR A vs C OR A vs D OR any two.
If balanced replace one of them.
If not balanced also replace one of them.
Then weigh it again and draw a conclusion. 

![down to 4 coins](images/coinproblem2.JPG "Coin problem")

Now try it with 9 coins at 3 weighs and 13 coins at 4 weighs.
[Solution](https://en.wikipedia.org/wiki/Balance_puzzle)

## Truth Tables

The most primitive operators are NOT, AND, and OR, where AND and OR require two input variables and NOT inverts a value. Here is a link to some [tables](https://medium.com/i-math/intro-to-truth-tables-boolean-algebra-73b331dd9b94).

## Converting number systems

These wiki links should sacrifice.
[1.](https://www.wikihow.com/Convert-from-Decimal-to-Binary)
[2.](https://www.electronics-tutorials.ws/binary/bin_2.html)
[3.](https://www.wikihow.com/Convert-from-Binary-to-Decimal)