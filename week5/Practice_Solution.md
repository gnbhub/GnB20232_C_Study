# ✅ Week 4 Practice Problem Solutions


### 1️⃣ 대소문자 바꾸기 (https://school.programmers.co.kr/learn/courses/30/lessons/181949)
```c
#include <stdio.h>
#define LEN_INPUT 20

// 한 글자씩 받아와 변환 후 반환
char change(char a){
  if ((65 <= a)&&(a <= 90)){
    a = a + 32;
  }
  else if ((97 <= a)&&(a <= 122)){
    a = a - 32;
  }
  return a;
}

// 배열을 인자로 받아와 각 인덱스에 접근해 변환값을 출력
void change2(char a[]){
  for (int i = 0; a[i]!='\0'; i++){
    if ((65 <= a[i])&&(a[i] <= 90)){
      printf("%c", a[i] + 32);
    }
    else if ((97 <= a[i])&&(a[i] <= 122)){
      printf("%c", a[i] - 32);
    }
  }
}

int main(void) {
    char s1[LEN_INPUT];
    scanf("%s", s1);
    for (int i = 0; s1[i]!='\0'; i++){
      printf("%c", change(s1[i]));
    }
    printf("\n");
    change2(s1);
    return 0;
}
```



### 2️⃣ 덧칠하기 (https://school.programmers.co.kr/learn/courses/30/lessons/161989)
```c

```
