---
weight: 4
title: Constants
date: 2021-05-24T06:15:02.696Z
lastmod: 2021-05-24T06:15:02.775Z
draft: false
author: codephilosopher
authorLink: "#"
tags:
  - golang
  - constants
categories:
  - Markdown
lightgallery: true
toc:
  auto: false
---
In Golang, we use the term `constant` to represent fixed (unchanging) values such as `5`, `1.34`, `true`, `"Hello"` etc.

**Literals are constants**

All the literals in Golang, be it integer literals like `5`, `1000`, or floating-point literals like `4.76`, `1.89`, or boolean literals like `true`, `false`, or string literals like `"Hello"`, `"John"` are **constants**.



| Constants                | Examples              |
| ------------------------ | --------------------- |
| integer constants        | `1000`, `67413`       |
| floating-point constants | `4.56`, `128.372`     |
| boolean constants        | `true`, `false`       |
| rune constants           | `'C'`, `'ä'`          |
| complex constants        | `2.7i`, `3 + 5i`      |
| string constants         | `"Hello"`, `"Rajeev"` |



**Declaring a Constant**

Literals are constants without a name. To declare a constant and give it a name, you can use the `const` keyword like so -



```go
const myFavLanguage = "Python"
const sunRisesInTheEast = true

```