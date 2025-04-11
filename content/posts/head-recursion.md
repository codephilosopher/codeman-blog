---
weight: 3
title: Head Recursion
date: 2022-11-20T16:27:48.928Z
lastmod: 2022-11-20T16:27:48.945Z
draft: true
author: codephilosopher
authorLink: https://codephilosopher.netlify.app/about/
tags:
  - go
categories:
  - algorithms
lightgallery: true
toc:
  auto: true
---
### intro 

In Head Recursion, the function call its self and function call will be the first statement than any other statement.

### code example

```go
package main

import "fmt"

func main() {
	x := 3
	recFunc(x)
}

func recFunc(n int) {
	if n > 0 {
		recFunc(n - 1)
		fmt.Printf("%d ", n)
	}
}
```

In the above example code, inside the if condition recFunc is the first statement. Then the recursive call will start and goes down until "n" turns to zero. When n equal to zero recursive call stops and return back from bottom to top. while returning back on each stack frames rest of the statement will execute. Here while return back print statement will print one first and delete the stack frame then goes one frame up and continues the procedure until there are no stack frame left to evaluate. 

so the output of this code will be 1,2,3.

![recursion](/images/uploads/screenshot-from-2022-11-20-22-16-44.png "head recursion")