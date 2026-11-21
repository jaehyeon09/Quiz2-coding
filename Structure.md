```
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
struct S {
    int k, e, m;
};
int main(void) {
    struct S a[3] = {
        {80, 90, 85},
        {70, 75, 95},
        {95, 85, 90}
    };
    FILE *p = fopen("my.bin", "wb");

    if (p == NULL) {
        printf("파일 생성 실패\n");
        return 1;
    }

    fwrite(a, sizeof(struct S), 3, p);
    fclose(p);
    printf("3명의 성적을 my.bin에 저장했습니다.\n");
    return 0;
}
```
### 기존 학생 2명의 성적을 3명으로 늘렸습니다.
### 바이너리 파일에 저장하는 학생 수를 2명에서 3명으로 변경했습니다.
### 수정 이유 : 기존 2명의 성적만 저장하던 프로그램을 3명의 성적을 저장하도록 변경하여 바이너리 파일에 더 많은 학생 정보를 저장할 수 있도록 했습니다.
