---
layout: post
title:  "Making Your Own Shell!"
date:   2021-02-27 12:22:45
categories: unix programming
---

Assembly language(asm) is a low-level programming language, where the language instructions will be more similar to machine code instructions

Here is a sample program that prints hello world in assembly, kindly taken from the internet

{% highlight cpp %}
section .data
	hello:     db 'Hello world!',10    ; 'Hello world!' plus a linefeed character
	helloLen:  equ $-hello             ; Length of the 'Hello world!' string

section .text
	global _start

_start:
	mov eax,4            ; The system call for write (sys_write)
	mov ebx,1            ; File descriptor 1 - standard output
	mov ecx,hello        ; Put the offset of hello in ecx
	mov edx,helloLen     ; helloLen is a constant, so we don't need to say
	                     ;  mov edx,[helloLen] to get it's actual value
	int 80h              ; Call the kernel
	mov eax,1            ; The system call for exit (sys_exit)
	mov ebx,0            ; Exit with return "code" of 0 (no error)
	int 80h;
{% endhighlight %}

ask yourself what are those 3 letter words that represent registers doing?
