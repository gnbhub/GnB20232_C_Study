## 1
```c
#include <stdio.h>
#define _CRT_SECURE_NO_WARNINGS
int main(void) {

  int i, num;
  int result = 1;
  int num2=1;
  printf("정수를 입력하세요 : ");
  scanf("%d", &num);

  for(i=1; i<=num; i++){
    result *=i;
    if(result*i/i != result){
      num2=0;
      printf("오버플로우 발생. 다른 수를 입력하세요.");
      break;
    }
  }
  if(num2==1){
    printf("%d! = %d", num, result);
  }
  
  return 0;
}
```
![image](https://github.com/gnbhub/GnB20232_C_Study/assets/127826727/f6ef1a38-c776-45a7-b7de-0f3c68b4f1ba)
![image](https://github.com/gnbhub/GnB20232_C_Study/assets/127826727/96b91d3d-0131-49af-a02e-0e030d4aba3a)

## 2
```c
#include <stdio.h>

int main(void)
{
    int num, i;
    scanf_s("%d", &num);
    int m = num / 4;
    if (num < 4 || num>1000) {
        printf("4~1000사이의 값을 입력하세요.");
    }
    else if(num % 4 != 0) {
        printf("4의 배수를 입력하세요.");
    }
    else {
        for (i = 0; i < m; i++)
        {
            printf("long ");
        }
        printf("int");
    }
 
    return 0;
}
```
![image](https://github.com/gnbhub/GnB20232_C_Study/assets/127826727/e844f1ec-5e5b-48f7-a98f-ed61813982ed)
![image](https://github.com/gnbhub/GnB20232_C_Study/assets/127826727/facf2778-5836-401d-a120-db8cf5e15a7a)
![image](https://github.com/gnbhub/GnB20232_C_Study/assets/127826727/d4900f3f-e45e-48e6-8805-1ef01c41cba9)

## 3
```c
#include <stdio.h>
#define _CRT_SECURE_NO_WARNINGS
int main(void) {
    int num, i, j;

    while (1) {
        printf("수를 입력 : ");
        scanf_s("%d", &num);

        if (num % 2 == 0) {
            printf("오류! 홀수를 입력하세요.\n");
        }
        else {
            for (i = 0;i <= num / 2;i++) {
                for (j = num / 2;j > i;j--) {
                    printf(" ");
                }
                for (j = 0;j < 2 * i + 1;j++) {
                    printf("*");
                }
                printf("\n");
            }
            for (i = 1;i <= num / 2;i++) {
                for (j = 0;j < i;j++) {
                    printf(" ");
                }
                for (j = num;j > 2 * i;j--) {
                    printf("*");
                }
                printf("\n");
            }
        }
    }
    return 0;
}
```
![image](https://github.com/gnbhub/GnB20232_C_Study/assets/127826727/ed0c349f-e3b6-412f-8e86-c58e9b7f2338)
