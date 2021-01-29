---
layout: post
title:  "Tech XiaBB"
date:   2021-01-12 11:02:24
category: tech
---

### 2021-01-29

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
