---
weight: 5
title: Recursion
date: 2022-07-23T06:14:44.785Z
lastmod: 2022-07-23T06:14:44.799Z
draft: false
author: codephilosopher
authorLink: https:/github.com/codephilosopher/codeman-blog
tags:
  - recursion
categories:
  - Algorithms
lightgallery: true
toc:
  auto: true
---
# **Recursion**

> * Definition: A function calling itself
> * There must be a base condition for exit the recursion else this will become a infinite recursion.
> * Recursion works like a tree structure.                                                                                                                                        



example program for recursive function:

```go
package main

import "fmt"

func recFunc(n int) {
  if n > 0 {
    fmt.Println(n)
    recFunc(n-1)
  }
}

func main() {
  x := 3
  recFunc(x)
}
```