## 1-1.
```c
#include <stdio.h>

int main(void) {
	printf("Hello World\n");
	return 0;
}
```

## 1-2.
```c
#include <stdio.h>

int main(void) {
	int a=10;
    	float b=5.2; 
    	char c='A';
    	char str01[]="GnB C Study";

    	printf("정수 : %d\n", a);
    	printf("소수 : %.1f\n", b);
    	printf("문자 : %c\n", c);
    	printf("문자열 : %s\n", str01);

    	return 0;
}
```

## 1-3.
```c
#include <stdio.h>
#define _CRT_SECURE_NO_WARNINGS

int main(void) {

	int num;
	printf("양의 정수를 입력하시오 : ");
	scanf_s("%d", &num);
	printf("|number\t|deciaml|octal\t|hexadecimal|\n");
	printf("|%d\t|%+d%\t|%o\t|%-11x|", num, num, num, num);
	return 0;
    }
```
