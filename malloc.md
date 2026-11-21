```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
    int *p = (int *)malloc(3 * sizeof(int));
    int s = 0;

    if (p == NULL) {
        printf("메모리 할당 실패\n");
        return 1;
    }

    p[0] = 11;
    p[1] = 33;
    p[2] = 55;

    for (int i = 0; i < 3; i++) {
        s += p[i];
        printf("숫자 %d: %d\n", i + 1, p[i]);
    }

    printf("전체 합계: %d\n", s);

    free(p);

    return 0;
}
```
### 메모리 할당이 제대로 되었는지 확인하는 조건문과 저장된 숫자를 출력하는 기능을 추가했습니다.
### if (p == NULL)을 추가하여 메모리 할당에 실패했을 때 오류 메시지를 출력하도록 변경했습니다.
### 반복문 안에 printf()를 추가하여 저장된 정수 3개를 확인할 수 있도록 했습니다.
