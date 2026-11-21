```
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    if (argc != 3) {
        printf("숫자 2개를 입력하세요.\n");
        return 1;
    }

    int a = atoi(argv[1]);
    int b = atoi(argv[2]);

    printf("두 수의 합: %d\n", a + b);
    printf("두 수의 차이: %d\n", a - b);

    return 0;
}
```
### 입력값이 2개인지 확인하고 잘못된 입력을 검사하는 코드를 추가했습니다.
### 기존 합계 출력에 두 수의 차이를 출력하는 기능을 추가했습니다.
### 수정 이유 : if (argc != 3) 조건문을 추가하여 숫자 2개가 입력되었는지 확인하도록 하였습니다.
