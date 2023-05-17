# 10wnck
```c
#include<stdlib.h>
#include<stdio.h>
#include<time.h>

int coin_toss(void);

int main(void)
{
  int toss; //동전 던지는 횟수를 나타내는 변수
  int heads = 0; //동전 앞면이 나오는 횟수를 나타내는 변수
  int tails = 0; //동전 뒷면이 나오는 횟수를 나타내는 변수
  srand((unsigned)time(NULL));

  //동전을 100번 던지는 반복문
  for (toss = 0; toss < 100; toss++)
  {
    //함수를 호출하고 반환값이 1이면 heads를 1 증가시킴
    if (coin_toss() == 1)
      heads++;
    //반환값이 0이면 tails를 1 증가시킴
    else
      tails++;
  }

  //동전의 앞면과 뒷면이 나온 횟수를 출력함
  printf("동전의 앞면: %d \n", heads);
  printf("동전의 뒷면: %d \n", tails);
  return 0;
}

int coin_toss( void )
{
  int head = rand() % 2;
  return head; //생성된 변수 값을 반환함
}
```
