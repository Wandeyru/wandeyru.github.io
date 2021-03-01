---
layout: post
title:  "Making Your Own Shell!"
date:   2021-02-27 12:22:45
categories: unix programming
---

This is the first in many posts in creating your own unix shell, lets call it sesh, get it. You might even think its short for session

This is a sample bullshit program writtenin c which uses recursion, try to guess the output:

{% highlight asm %}
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

int main(int argc, char* argv[])
{
    foo(30);
}
{% endhighlight %}

Is it possible to make this code work in a better way, are there any optimizations?
