---
weight: 3
title: Recursion
date: 2022-11-20T07:57:49.728Z
lastmod: 2022-11-20T07:57:49.740Z
draft: false
author: codephilosopher
authorLink: https:/github.com/codephilosopher/codeman-blog
tags:
  - go
categories:
  - algorithms
lightgallery: true
toc:
  auto: false
---
**I﻿ntro**

recursion is a method of solving a computational problem where the solution depends on solutions to smaller instances of the same problem. Recursion solves such recursive problems by using functions that call themselves from within their own code 

Repeatedly calling a function from within itself may cause the call stack to have a size equal to the sum of the input sizes of all involved calls. It follows that, for problems that can be solved easily by iteration, recursion is generally less efficient, and, for large problems, it is fundamental to use  optimization techniques such as tail call optimization.[](recursion)

\-Wiki

consider an example:

```go
import "fmt"

func main() {
	SimpleRecursion(3)
}

func SimpleRecursion(n int) {
	if n > 0 {
		fmt.Println(n)
		SimpleRecursion(n - 1)
	}
	return
}
```