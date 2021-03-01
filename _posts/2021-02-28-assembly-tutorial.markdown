---
layout: post
title:  "Introductory Assembly Tutorial"
date:   2021-02-28 11:50:25
categories: unix programming
---


Assembly language(asm) is a low-level programming language, where the language instructions will be more similar to machine code instructions

Here is a sample program that prints hello world in assembly, kindly taken from the internet

{% highlight as %}
section .data
    hello:     db 'Hello world!',10    
	helloLen:  equ $-hello            

section .text
	global _start

_start:
	mov eax,4            
	mov ebx,1            
	mov ecx,hello       
	mov edx,helloLen     
	int 80h           
	mov eax,1       
	mov ebx,0           
	int 80h;
{% endhighlight %}

ask yourself what are those 3 letter words that represent registers doing?
