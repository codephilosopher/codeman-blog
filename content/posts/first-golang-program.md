---
weight: 5
title: first golang program
date: 2022-07-10T10:21:05.958Z
lastmod: 2022-07-10T10:21:05.980Z
draft: false
author: codephilosopher
authorLink: https:/github.com/codephilosopher/codeman-blog
tags:
  - golang
categories:
  - programming
lightgallery: true
toc:
  auto: false
---
It is the custom to start a program by printing "Hello World!" 😊

`package main`

`import "fmt"`

`func main() {`

`         fmt.Println("Hello World!")`

`} ` 

* Every Go program starts with a package name, This is a main program with drives other programs, so this has the main package. 
* ***func main***   is the entry point to go program for operating system. from this main function all other programs are called and executed.
* functions have opening and closing curly braces. Inside the main function, we write all other code. 
* ***fmt*** is a package name like main, inside package name directory,  a group of similar related functions are grouped under a package name. Here ***Println*** function is put under ***fmt*** package. ***fmt.Println()***  will print to the standard out streams like terminal.