---
title: "# Problem 01"
layout: page
---

## 다음 C 코드의 실행 결과는?

```c
#include <stdio.h>

int main() {
    int a[3] = {4, 5, 6};
    int (*p)[3] = &a;
    printf("%d\n", (*p)[0]);
    return 0;
}
```

1. 컴파일 에러
2. Segmentation Fault
3. 4가 출력됨
