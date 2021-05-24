---
weight: 4
title: sample
date: 2021-05-24T05:52:05.676Z
lastmod: 2021-05-24T05:52:05.754Z
draft: false
author: codephilosopher
authorLink: https:/github.com/codephilosopher/codeman-blog
tags:
  - java
categories:
  - Markdown
lightgallery: true
toc:
  auto: false
---


```java
public class Largest {

    public static void main(String[] args) {

        double n1 = -4.5, n2 = 3.9, n3 = 2.5;

        if( n1 >= n2 && n1 >= n3)
            System.out.println(n1 + " is the largest number.");

        else if (n2 >= n1 && n2 >= n3)
            System.out.println(n2 + " is the largest number.");

        else
            System.out.println(n3 + " is the largest number.");
    }
}
```