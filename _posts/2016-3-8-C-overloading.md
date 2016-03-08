---
layout: post
published: true
exacttime: "23:00:00"
title: "Function overloading in C"
category: "C"
author: shreyashpatodia
---

Greetings everyone !!

Have you ever looked at the printf function in C and thought, if C doesn't support overloading how does it take different number of arguments to printf.

Now the topic of function of overloading in C is one that I find very interesting since it does not support overloading(well, it kind of does now ! Read on for more) in a traditional Java-like way. But by messing around a little bit we can learn some really cool ways to implement the same(read:similar) functionality. 


The first way to get the effect of overloading is by using an array of function pointers. An example to a program that uses this is this implementation of finding the nth fibonacci number: 


{% gist ShreyashPatodia/b5f41a957f59214c30fe %}


Although, not strictly equivalent to function overloading creating an array of functions that do the same task gives a clear idea of the relationships between the functions. We don't even need to have different parameter lists in order for the program to know it needs to implement different functions. Moreover we can code-up a Java-like like implementation using the fact that argv tells us the number of command line inputs to the program so we can use it to implement different functions in an array of functions.


Moving on, the other method to do overloaded functions in C is to use _Generic. Using _Generic is the closest thing to function-overloading that C can offer. It allows us to list a number of possibilities for a argument to a function and take action accordingly. For example: 

{% gist ShreyashPatodia/a74f53d8ad61787086ec %}


Lastly, C uses something varargs to do implement the previously mentioned printf function where the idea is to take a char * input in order to allow variable argument lists. 
Here is the version of GNU version of the printf function:

{% gist ShreyashPatodia/081db16685e300b26076 %}

Note: printf is not the real function implementing the printing, vfprintf does all the heavy-lifting. So there is not much to see up there.



