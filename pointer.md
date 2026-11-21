```
#include <stdio.h>
int multiply(int a, int b) {
    return a * b;
}
int main(void) {
    int a = 11, b = 22;
    int (*sum)(int, int) = multiply;
    printf("두 수의 곱: %d\n", sum(a, b));
    return 0;
}
```
## 기존 덧셈 함수 add()를 곱셈 함수 multiply()로 변경했습니다.
## 수정이유 : 함수 포인터가 단순히 덧셈 함수뿐만 아니라 곱셈 함수도 가리킬 수 있다는 것을 확인하기 위해 함수를 변경했습니다.
