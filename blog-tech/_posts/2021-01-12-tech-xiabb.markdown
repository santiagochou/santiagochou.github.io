---
layout: post
title:  "Tech XiaBB"
date:   2021-01-12 11:02:24
category: tech
---

### 2021-01-29
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
