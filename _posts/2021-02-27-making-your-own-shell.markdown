---
layout: post
title:  "Making Your Own Shell!"
date:   2021-02-27 12:22:45
categories: unix programming
---

This is the first in many posts in creating your own unix shell, lets call it sesh, get it. You might even think its short for session

This is a sample bullshit program writtenin c which uses recursion, try to guess the output:

{% highlight c %}
#include <stdio.h>
#include <unistd.h>
#include <sys/syscall.h>
void foo(int c) {
    if( c == 1) {
        return 1;
        printf("At the base case.\n");
    } else {
        return c + foo( c - 1 );
    }
}
{% endhighlight %}

Is it possible to refactor this code so it does something very similar, what is the cost of running this program?.
