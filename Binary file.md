```
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>

struct S {
    int k, e, m;
};
int main(void) {
    struct S a[3];
    FILE *p = fopen("my.bin", "rb");
    if (p == NULL) {
        printf("파일을 열 수 없습니다.\n");
        return 1;
    }
    if (fread(a, sizeof(struct S), 3, p) != 3) {
        printf("파일 읽기 실패\n");
        fclose(p);
        return 1;
    }
    fclose(p);

    for (int i = 0; i < 3; i++) {
        printf("학생 %d 평균: %.2f\n",
            i + 1, (a[i].k + a[i].e + a[i].m) / 3.0);
    }
    printf("국어 평균: %.2f\n",
        (a[0].k + a[1].k + a[2].k) / 3.0);

    printf("영어 평균: %.2f\n",
        (a[0].e + a[1].e + a[2].e) / 3.0);

    printf("수학 평균: %.2f\n",
        (a[0].m + a[1].m + a[2].m) / 3.0);

    return 0;
}
```
### 기존 학생 2명의 성적을 읽던 코드를 3명의 성적을 읽도록 변경했습니다.
### 학생별 평균과 과목별 평균을 계산하도록 수정했습니다.
### 파일이 존재하지 않을 경우 오류 메시지를 출력하도록 추가했습니다.
### 수정 이유 : 3명의 성적을 모두 읽을 수 있도록 변경했습니다. 또한 학생별 평균과 과목별 평균을 출력하도록 하여 성적 분석 기능을 추가했습니다.
