---
weight: 3
title: Tail Recursion
date: 2022-11-21T12:28:03.093Z
lastmod: 2022-11-21T12:28:03.111Z
draft: false
author: codephilosopher
authorLink: https:/github.com/codephilosopher/codeman-blog
tags:
  - go
categories:
  - algorithms
lightgallery: true
toc:
  auto: true
---
### I﻿nto 

In Tail Recursion, recursive call is the last statement to be executed by the function. In other words, recursive function will put at the end of the function. So here all other statements are executed on the recursive calling time itself because all other statements are called before the recursive function. So there wont be anything executed after returning time of the recursive call.

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
		fmt.Printf("%d ", n)
		recFunc(n - 1)
	}
}
```

in the above example you can see print statement is before recursive function, so before on each recursive call print statement executed first and in the returning time there wont be anything left to executed.

The output will be in descending order unlike head recursion.