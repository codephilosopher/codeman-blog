---
weight: 1
title: Two Pair Sum
date: 2025-04-10T06:18:05.953Z
lastmod: 2025-04-10T06:18:05.971Z
draft: false
author: codephilosopher
authorLink: https:/github.com/codephilosopher/codeman-blog
tags:
  - Go
categories:
  - DSA
lightgallery: true
toc:
  auto: false
---
\#﻿pairs

Given an array containing N integers and an number S denoting a target Sum.

Find two distinct integers that can pair up to form target sum.  Let us assume there will be only one such pair.

**Input**:

`a﻿rray = [10, 5, 2, 3, -6, 9, 11 ]`

`S﻿ = 4`

**output**:

`[﻿10, -6]`

*Solution*:

### Naive Approach:

We can use two loops which will compare each element with other elements that gives the sum. This will take an order of O(n^2).

**O﻿ptimal Approach O(N) :**

I﻿n this approach we will avoid one loop, instead of comparing the second value with a loop, we will use a map to lookup the subtracted value from the total sum. Map will take only a constant time to lookup the value. So the total running time of this approach will be order of O(N).

```go
package main

import "fmt"

type Pair struct {
	a int
	b int
}

func main() {
	arr := []int{10, 5, 2, 3, -6, 9, 11}
	p := pairSum(arr, 4)
	fmt.Println(p)
}

func pairSum(a []int, s int) Pair {
	indexMap := map[int]int{}
	for i, v := range a {
		indexMap[v] = i
	}
	for i, v := range a {
		if index, ok := indexMap[s-v]; ok {
			if index != i {
				return Pair{a[i], a[index]}
			}
		}
	}
	return Pair{-1, -1}
}

```