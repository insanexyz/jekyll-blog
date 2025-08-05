---
layout: post
title: Detect datatype of variables in C
date: 2025-06-22
categories: C
author: insane
permalink: /posts/detect-datatype-of-variables-using-generics
tags: c programming typeof generics
---

![Thumbnail for the post](/assets/detect-datatype-of-variables-in-c-using-generics/thumbnail.webp)

A simple Marco which uses generics in C to help you detect data type of any variable like you do with type() function in python :] .

The code snippet contains examples on how to use it.  
Extend it as much as you like!

```c
#include <stdio.h>
#include <stdlib.h>

#define TYPE_CHECK(var) _Generic((var),     \
    int             : "int",                \
    float           : "float",              \
    double          : "double",             \
    char            : "char",               \
    char*           : "string",             \
    int*            : "int pointer",        \
    float*          : "float pointer",      \
    double*         : "double pointer",     \
    char**          : "string pointer",     \
    void*           : "void pointer",       \
    short           : "short",              \
    long            : "long",               \
    unsigned int    : "unsigned int",       \
    unsigned long   : "unsigned long",      \
    unsigned short  : "unsigned short",     \
    default         : "unknown type"        \
)

int main(void) {
    // Basic types
    int a = 10;
    float b = 5.5f;
    double c = 3.14159;
    char d = 'A';
    char* str = "Hello, World!";
    
    // Pointer types
    int* p_a = &a;
    float* p_b = &b;
    double* p_c = &c;
    char** p_str = &str;
    void* p_void;

    // Print types using TYPE_CHECK
    printf("Type of a: %s\n",       TYPE_CHECK(a));         // Outputs "int"
    printf("Type of b: %s\n",       TYPE_CHECK(b));         // Outputs "float"
    printf("Type of c: %s\n",       TYPE_CHECK(c));         // Outputs "double"
    printf("Type of d: %s\n",       TYPE_CHECK(d));         // Outputs "char"
    printf("Type of str: %s\n",     TYPE_CHECK(str));       // Outputs "string"
    printf("Type of p_a: %s\n",     TYPE_CHECK(p_a));       // Outputs "int pointer"
    printf("Type of p_b: %s\n",     TYPE_CHECK(p_b));       // Outputs "float pointer"
    printf("Type of p_c: %s\n",     TYPE_CHECK(p_c));       // Outputs "double pointer"
    printf("Type of p_str: %s\n",   TYPE_CHECK(p_str));     // Outputs "string pointer"
    printf("Type of p_void: %s\n",  TYPE_CHECK(p_void));    // Outputs "void pointer"

    // Example of using malloc
    void* ptr = malloc(sizeof(int));
    printf("Type of ptr: %s\n",     TYPE_CHECK(ptr));       // Outputs "void pointer"

    // Good practice :)
    free(ptr);
    
    return 0;
}
```

🦖