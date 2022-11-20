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
  auto: true
---
### I﻿ntro

recursion is a method of solving a computational problem where the solution depends on solutions to smaller instances of the same problem. Recursion solves such recursive problems by using functions that call themselves from within their own code 

Repeatedly calling a function from within itself may cause the call stack to have a size equal to the sum of the input sizes of all involved calls. It follows that, for problems that can be solved easily by iteration, recursion is generally less efficient, and, for large problems, it is fundamental to use  optimization techniques such as tail call optimization.[](recursion)

\-Wiki

### code example:

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
}
```

Every recursive program should contain a precondition to exit from the program, In the above example the main condition only works when "n" is greater than zero and inside the condition there is the recursion call SimpleRecursion which calls the function calls itself. on each call n is reduced by one. When n become zero recursion will stop and main program will stop.

### recursion side effects

There are side effects for using Recursion, every function uses stack memory to compute, Internally recursion uses stack memory on each recursive call. The stack memory created according to the growth of n, so the space complexity of a recursive function is order of n **O(n).** 

![call stack](/images/uploads/screenshot-from-2022-11-20-18-03-16.png "recursion call stack")



### s﻿tackoverflow

```
runtime: goroutine stack exceeds 1000000000-byte limit
runtime: sp=0xc020160370 stack=[0xc020160000, 0xc040160000]
fatal error: stack overflow
```

Another downside of using recursion is not proper using of precondition, this will lead to stack overflow. This happens because of the indefinite recursive function call.