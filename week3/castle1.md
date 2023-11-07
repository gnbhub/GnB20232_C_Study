```c
#include <stdio.h>

unsigned long long factorial(int n) {
    if (n == 0 || n == 1) {
        return 1; // 0!과 1!은 1이다.
    }

    unsigned long long result = 1;
    for (int i = 2; i <= n; i++) {
       if (result > ULLONG_MAX / i) {
            return 0; 
        }
        result *= i;
    }
    return result;
}

int main() {
    int n;


    printf("정수 n을 입력하세요: ");
    scanf("%d", &n);

    unsigned long long result = factorial(n);

    if (result == 0) {
        printf("오버플로우가 발생했습니다. 다른수를 입력하세요.\n");
    } else {
        printf("%d! = %llu\n", n, result);
    }

    return 0;
}
```

```c
#include <stdio.h>

int main() {
    int n;

    while (1) {
        printf("수를 입력: ");
        scanf("%d", &n);

        if (n % 2 == 0 || n <= 0) {
            printf("홀수를 입력하세요.\n");
        } else {
            break;
        }
    }

    int i, j, k;

    for (i = 1; i <= n; i += 2) {
        for (k = 0; k < (n - i) / 2; k++) {
            printf(" ");
        }
        for (j = 1; j <= i; j++) {
            printf("*");
        }
        printf("\n");
    }

    for (i = n - 2; i >= 1; i -= 2) {
        for (k = 0; k < (n - i) / 2; k++) {
            printf(" ");
        }
        for (j = 1; j <= i; j++) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}
```
