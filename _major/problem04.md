---
title: "# Problem 04"
layout: page
---

## C++17 표준하에서 아래 코드가 성공적으로 컴파일되기 위해 빈칸에 들어갈 알맞은 코드 조합은?

```c++
void (*signal(int _, void (*)(int)))(int) {
    return SECRET; // This macro expands to the appropriate return value
}

int main() {
    ____ = signal(____);
    return 0;
}
```

- 보기 (빈칸별로 서로 다른 행 선택 가능, e.g. 첫 번째 빈칸 (a), 두 번째 빈칸 (b))

  |     |    첫 번째 빈칸    |                   두 번째 빈칸                    |
  | :-: | :----------------: | :-----------------------------------------------: |
  | (a) |     `void fp`      |               `0, [] { return 0; }`               |
  | (b) |     `void *fp`     |            `0, [](int x) { return; }`             |
  | (c) | `void (*fp)(int)`  |        `&(int){0}, [](int x) { return; }`         |
  | (d) | `void *(*fp)(int)` |       `0, [](int x) { return &(int){0}; }`        |
  | (e) |        기타        | 위 보기와는 전혀 다른 형태의 정답을 떠올리셨다면? |
