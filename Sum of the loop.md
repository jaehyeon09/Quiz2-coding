```
#include <stdio.h>

int main(void) {
    int i = 5;
    int s = 0;
    int count = 0;

    while (i <= 10) {
        s += i;
        i++;
        count++;
    }

    printf("5부터 10까지의 합: %d\n", s);
    printf("반복 횟수: %d\n", count);

    return 0;
}
```
### 기존 for문을 while문으로 변경하고 반복 횟수도 출력하도록 추가했습니다.
### 합계뿐만 아니라 반복 횟수도 확인할 수 있도록 기능을 추가했습니다.
### 수정 이유 : count 변수를 추가하여 반복문이 실행된 횟수를 계산하도록 하기 위해 수정하였습니다.
