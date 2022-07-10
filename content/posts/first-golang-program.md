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

```go
package main

import "fmt"

func main() {
	fmt.Println("Hello World!")
}
```

* Every Go program starts with a package name, This is a main program which drives other programs, so this has the main package name. 
* ***func main***   is the entry point to go program for operating system. From this main function, all other programs are called and executed.
* Functions have opening and closing curly braces. Inside the main function, we write all other code. 
* ***fmt*** is a package name like main,  a group of similar related functions are grouped under a package name directory. Here ***Println*** function is put under ***fmt*** package. ***fmt.Println()***  will print to the standard out streams like terminal.
* ***import "fmt"*** is the package import statement in Go, We can import multiple package import declaration in side a opening and closing parenthesis.
* To run a go program, we need to type and enter these line of code in your terminal `go run source_file.go` 

you can get the source code from here [hello world program](https://raw.githubusercontent.com/codephilosopher/golang_playlist_youtube/master/first%20program%20hello%20world/hello.go)   

Also you can watch video explanation of this from codephilosopher's youtube channel. [hello world](https://www.youtube.com/watch?v=MzwDk2bOybo)