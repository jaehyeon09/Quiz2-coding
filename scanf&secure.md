```
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <string.h>
 
void main(void) {
char str[200];
printf("문장 입력: ");
scanf("%[^\n]", str); // 엔터(\n) 전까지 공백 포함 문장 전체 입력

// 문자열 끝에서부터 거꾸로 한 글자씩 출력
for (int i = (int)strlen(str) - 1; i >= 0; i--) {
printf("%c", str[i]);
}
}
```
## 문자열 배열 크기를 100에서 200으로 늘렸습니다.
## 배열 크기를 더 늘려서 더 긴 문장을 입력할 수 있도록 하였다.
