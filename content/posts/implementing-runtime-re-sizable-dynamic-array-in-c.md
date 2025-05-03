---
weight: 1
title: Implementing runtime-re-sizable dynamic array in C
date: 2025-05-03T04:27:20.587Z
lastmod: 2025-05-03T04:27:20.598Z
draft: false
author: codephilosopher
authorLink: https:/github.com/codephilosopher/codeman-blog
tags:
  - C
categories:
  - array
lightgallery: true
toc:
  auto: false
---
You can implement your own dynamic array using `malloc`, `realloc.`   

```c
#include <stdio.h>
#include <stdlib.h>

typedef struct {
  int *data;
  size_t size;
  size_t capacity;
} DynamicArray;

void initArray(DynamicArray *arr, size_t initialCapacity){
    arr->data = (int*)malloc(initialCapacity*sizeof(int));
    arr->size = 0;
    arr->capacity = initialCapacity;
}

void resizeArray(DynamicArray *arr, size_t newCapacity) {
    arr->data = (int*)realloc(arr->data, newCapacity*sizeof(int));
    arr->capacity = newCapacity;
}

void addElement(DynamicArray *arr, int element) {
    if (arr->size >= arr->capacity) {
        resizeArray(arr, arr->capacity*2);
    }
    arr->data[arr->size++] = element;
}

void freeMem(DynamicArray *arr) {
    free(arr->data);
    arr->data = NULL;
    arr->size = 0;
    arr->capacity = 0;
}

int main() {
    DynamicArray arr;
    initArray(&arr, 4);
    for (int i = 1; i <= 10; i++) {
        addElement(&arr, i*10);
    }

    for (size_t i = 0; i < arr.size; ++i) {
            printf("arr[%zu] = %d\n", i, arr.data[i]);
        }

    freeMem(&arr);
    return 0;
}
```