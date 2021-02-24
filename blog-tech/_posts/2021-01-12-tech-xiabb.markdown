---
layout: post
title:  "Tech XiaBB"
date:   2021-01-12 11:02:24
category: tech
---


### 2021-02-24

* gRPC+ProtoBuf -->实现Client-Server通信，而不用写基础的Client端和Server端的服务代码，直接关心其基础之上的业务逻辑。
* Bazel & Buck 是一个能够替代CMake的编译框架。

### 2021-02-08
#### Macros in VS Studio

* Macros in VStudio is the VS Studio Environment Variables. It can be found in the all of the page in the Property of the project.

### 2021-02-01
#### Operating System Kernel

* Kernel is the main component of any operating system. It is a bridge between applications and hardware. Kernel provides layer of abstraction through which application can interact with hardware. 

* See figure ![Operating System Kernel](/assets/images/tech/2021-01-12-tech-xiabb/2021-02-01.svg) 

* Kernel is the part of the operating system that loads first, and it remains in physical memory. The kernel's primary function is to manage the computer's hardware and resources and allow other programs to run and use these resources. To know more about kernel, visit [this link](https://en.wikipedia.org/wiki/Kernel_(operating_system))

### 2021-01-29
#### callback function in C:

* **callback** can define a function which accepts a sort of functions which perform a sort of actions.

``` C
/*
* refers to https://www.geeksforgeeks.org/callbacks-in-c/
*/
// A simple C program to demonstrate callback 
#include<stdio.h> 

void A()
{
    printf("I am function A\n");
}

// callback function 
void B(void (*ptr)())
{
    (*ptr) (); // callback to A 
}

int main()
{
    void (*ptr)() = &A;

    // calling function B and passing 
    // address of the function A as argument 
    B(ptr);

    return 0;
}

```

#### C++ volatile specifier

* 这个关键字是用来设定某个对象的存储位置在内存中，而不是寄存器中。因为一般的对象编译器可能会将其的拷贝放在寄存器中用以加快指令的执行速度.
* 当要求使用 volatile 声明的变量的值的时候，系统总是重新从它所在的内存读取数据，即使它前面的指令刚刚从该处读取过数据。 
* A volatile specifier is a hint to a compiler that an object may change its value in ways not specified by the language so that aggressive optimizations must be avoided.

#### new knowledge of struct. following is the example.
``` C++

#include <stdio.h>
struct _st{
    unsigned char flag : 4; // 4 is number of bits.
} st;

void main(void)
{
    st.flag = 15;
    printf("%d\n", st.flag); // 15
    st.flag = 16;
    printf("%d\n", st.flag); // 16
}

```

### 2021-01-12
#### Timing Generate Tools
* Timegen
* WaveDrom
* TimingDesigner
* Waveme
* tikz-timing
* TimingAnalyzer
