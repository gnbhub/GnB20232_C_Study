# ✏ Week 4 Practice Problem Solutions

### 1️⃣ 백준 10807 : 개수 세기 (https://www.acmicpc.net/problem/10807)
#### By 이유준
```c
#include <stdio.h>

int i, count, numset, findnum, input;

int main(){
    scanf("%d", &count);
    int numset[count];

    for(i = 0; i <  count; i++){
        scanf("%d", &input);
        numset[i] = input;
    }

    scanf("%d", &findnum);
    int ans = 0;

    for(i = 0; i < count; i++){
        if(numset[i] == findnum){
            ans++;
        }
    }
    printf("%d", ans);

    return 0;
}
```



### 2️⃣ 백준 10798 : 세로읽기
#### By 임재희
```c
#include <stdio.h>

int main(void) {
  char a[5][16] = {0};


  for(int i=0; i<5;i++)
    {
      scanf("%s",a[i]);
    }
  for(int j=0; j<16; j++)
    {
      for(int k=0; k<5; k++)
        {
          if(a[k][j]==NULL) continue;
          else
          {
          printf("%c",a[k][j]);
          }
        }
    }
}  
```
