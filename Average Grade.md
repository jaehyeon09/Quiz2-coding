```
#include <stdio.h>

typedef struct {
    char name[20];
    int kr, en;
} Stud;

int main(void) {
    Stud s[3] = {
        {"J.C. Shim", 90, 95},
        {"G.D. Hong", 80, 85},
        {"J.Y. Ko", 70, 75}
    };

    double total = 0;

    for (int i = 0; i < 3; i++) {
        double avg = (s[i].kr + s[i].en) / 2.0;

        printf("이름: %s\n", s[i].name);
        printf("국어: %d, 영어: %d\n",
            s[i].kr, s[i].en);
        printf("개인 평균: %.2f\n\n", avg);

        total += avg;
    }

    printf("전체 학생 평균: %.2f\n", total / 3);

    return 0;
}
```
### double total = 0;을 추가하여 학생들의 평균을 모두 더할 수 있도록 했습니다.
### total += avg;를 추가하여 각 학생의 평균을 누적하도록 변경했습니다.
### 마지막에 printf("전체 학생 평균: %.2f\n", total / 3);을 추가하여 3명의 전체 평균도 출력하도록 기능을 확장했습니다.
