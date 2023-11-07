```c
#include <stdio.h>
#include <math.h>

int main() {
    double x1, y1, x2, y2;

   
    printf("첫 번째 점의 x 좌표를 입력하세요: ");
    scanf("%lf", &x1);
    printf("첫 번째 점의 y 좌표를 입력하세요: ");
    scanf("%lf", &y1);
    printf("두 번째 점의 x 좌표를 입력하세요: ");
    scanf("%lf", &x2);
    printf("두 번째 점의 y 좌표를 입력하세요: ");
    scanf("%lf", &y2);

    
    if (x1 == x2 || y1 == y2) {
        printf("직사각형을 만들 수 없음.\n");
    } else {
        // 직사각형의 가로, 세로, 대각선 길이 계산
        double width = fabs(x2 - x1);  // 가로 길이
        double height = fabs(y2 - y1); // 세로 길이
        double diagonal = sqrt(width * width + height * height); // 대각선 길이
       
        double perimeter = 2 * (width + height); // 둘레 길이
        double area = width * height; // 넓이

        printf("직사각형의 둘레 길이: %.2lf\n", perimeter);
        printf("직사각형의 넓이: %.2lf\n", area);
        printf("대각선의 길이: %.2lf\n", diagonal);
    }

    return 0;
}

```


```c
#include <stdio.h>

int main() {
    double num1, num2, result;
    char operator;

    
    printf("두 숫자와 연산자를 입력하세요 (예: 2 + 3): ");
    if (scanf("%lf %c %lf", &num1, &operator, &num2) != 3) {
        printf("잘못된 입력 형식. 숫자 연산자 숫자 형태로 입력하세요.\n");
        return 1; // 오류 처리
    }

   
    switch (operator) {
        case '+':
            result = num1 + num2;
            break
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            if (num2 == 0) {
                printf("0으로 나눌 수 없습니다.\n");
                return 1; // 오류 처리
            }
            result = num1 / num2;
            break;
        default:
            printf("잘못된 연산자임. +, -, *, / 중 하나를 입력하세요.\n");
            return 1; // 오류 처리
    }

  
    printf("결과: %.2lf\n", result);

    return 0;
}
```


