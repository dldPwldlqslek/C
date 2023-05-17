10주차
# 동전 던지기
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
# 차의 이동 
```c
#include <stdlib.h>
#include <stdio.h>
#include <conio.h>
#include <time.h>

void disp_car(int car_number, int distance)
{
  int i;
  printf("CAR #%d:", car_number);
  
  for(i=0; i<distance/10; i++)
    {
      printf("*");
    }
  printf("\n");
}

int main(void)
{
  int i;
  int car1_dist=0, car2_dist=0;

  //시간에 따라 랜덤값을 생성하기 위해 srand() 함수를 사용함
  srand((unsigned)time(NULL));

  //6번을 반복해 차 2대의 이동 거리를 업데이트하고 표시함
  for(i=0; i<6; i++)
    {
      //차 2대의 이동 거리를 랜덤값으로 업데이트함
      car1_dist += rand() % 100;
      car2_dist += rand() % 100;
      
      //disp_car 함수를 호출해서 차 2대의 이동 거리를 표시함
      disp_car(1, car1_dist);
      disp_car(2, car2_dist);
      
      //차 2대의 이동 거리를 구분하기 위해 선을 출력함
      printf("------------------\n");
      
      _getch();
    }
  
  return 0;
}
```
