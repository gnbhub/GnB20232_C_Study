# ✏ Week 6
- Topic : 포인터
- context : 강의자료 10

## Practices

### 1️⃣ 연습문제
#### 문제

![image](https://github.com/gnbhub/GnB20232_C_Study/assets/51956616/837aeb2f-0e79-4f63-a4c7-ef26e6c81a23)


#### 답 : 8, 9
#### 왜 그런지 이유를 살펴보기

[11.28] ans) https://it-freelancer.tistory.com/846


### 2️⃣ 입력받은 문장을 거꾸로 출력
#### 문제
```
-배열에 문장을 입력할 것

-입력받은 배열을 거꾸로 변환하는 함수 만들기

-함수에서 출력하지 말고 main에서 출력하기

-문장 최대 길이는 30자
```
#### 입력
```
I am hungry
```
#### 출력
```
yrgnuh ma I
```

[11.28] ans)
```c
#include <stdio.h>

int main() {
    char input[100];
    char c;
    int index = 0;

    // 사용자로부터 문자열 입력 받기
    printf("문장을 입력하세요: ");

    // Enter 키가 입력될 때까지 문자 하나씩 입력 받음
    while ((c = getchar()) != '\n' && index < sizeof(input) - 1) {
        input[index++] = c;
    }

    // 널 문자를 배열 끝에 명시적으로 추가
    input[index] = '\0';

    // 문자열 뒤집기
    int length = index;
    char temp;
    for (int i = 0; i < length / 2; i++) {
        temp = input[i];
        input[i] = input[length - i - 1];
        input[length - i - 1] = temp;
    }

    // 뒤집힌 문자열 출력
    printf("거꾸로 된 문장: %s\n", input);

    return 0;
}
```
![image](https://github.com/gnbhub/GnB20232_C_Study/assets/51956616/9b60d18a-a348-49ab-8812-d8fa7f663fd9)
