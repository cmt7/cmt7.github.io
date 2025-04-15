---
title: "\"Minimalism\" is not an excuse for laziness"
date: 2024-11-15
author: "Christian Thackston"
---

## Introduction

I am an extensive proponent of the "suckless" software experience. I (used to) write my own website using pure html using Vim, I believe in the Unix philosophy, and all of my software can pull from stdin and output to stdout. I believe programs *do* need to be adaptable and extensible. I think the user should be able to use them as they see fit. I think projects like dwm and st are fantastic and do everything right (though I'm currently using Sway and Foot), but I see a recurring issue in modern software development that adopts this philosophy that puts a sour taste in my mouth.

## The Unix Philosophy

While I believe a program should be able to be used in a chain of pipes or the like, I don't like the idea of these programs requiring it. For example, we could implement 'cp' using only cat and shell redirects such as "cat file.txt > file_copy.txt", but things like this are never done because they simply take too long to write and frankly, are stupid, while only giving us a shred of usability (what about recursiveness?).

There is a reason the folks over at Bell Labs didn't use shell redirects for everything. Nobody complains that 'cp' breaches the Unix philosophy because that isn't what it stands for. The philosophy is "do one thing, and do it well". This doesn't mean one operation, but rather one task.

## The Problem with Modern Minimalism

I think the idea of an OS that has such immense modularity is cool idea but it would exist for the same reason [brainfuck](https://brainfuck.org/) exists. Breaking down things to their simplest components do not make things easier, and in the same way, modularity is only useful to a point, and I think this point is being surpassed by a number of modern "minimalist" software. There is obviously a conversation to be had about things that do the opposite, but these cases are so well documented that they are simply not worth mentioning.

I'm not gonna call out any names, but I think we've all come across it. Programs that claim to be "simple" while failing to accomplish their purpose. Programs should be used to accomplish a task, not be minimalist and nothing more. Programs can accomplish a task *and* be minimalist (see my above examples) but both of these conditions need to be met to create a useful program.

## Finding the Balance

Many programs that exist to accomplish simple tasks can be built using a bash script and existing tools (and many programs are basically scripts on top of large libraries), but there is a reason why we write software instead of doing so. We do it for efficiency and extensibility. Having to go through this script every time you need to do something new is absurd.

Programming is built on abstraction (who uses syscalls over libc?), but there is a point where the abstraction becomes so great that you're just writing a script, and that is pointless (not that scripts are pointless, but rather are not programs). These are too very different problems, but my point is: use enough abstraction to make the program useful, but not so much that you're just scripting.

Writing code in this "Goldilocks zone" is exactly how you create minimalist *and* useful software. Anywhere on either side, you make garbage.