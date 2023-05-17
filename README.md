10주차
# 동전 던지기 게임
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
# 자동차 게
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
# pow()와 sqrt()
```c
#include <math.h>
#include <stdio.h>

int main( void )
{ 
  double pi = 3.1415926535;
  double x, y;

  //x에 pi / 2 대입 후 x의 sin 값 계산
  x = pi / 2; 
  y = sin( x ); 

  //sin 값 출력
  printf( "sin( %f ) = %f\n", x, y ); 

  //x의 cos 값 계산
  y = cos( x ); 

  //cos 값 출력
  printf( "cos( %f ) = %f\n", x, y ); 
}
```
# 무제
```c
#include <stdlib.h>
#include <stdio.h>

int main(void)
{
  system("dir");

  //아무 키나 누를 때까지 대기한다는 안내 메시지 출력
  printf("아무 키나 치세요\n");

  //_getch 함수를 사용하여 사용자 입력 대기
  _getch();

  //화면을 지우는 cls 명령어 실행
  system("cls");

  return 0;
}
```
# 시간 맞추기 게임
```c
#include <stdio.h>
#include <time.h>

int main(void)
{
  time_t start, end;
  start = time(NULL);

  //10초가 되면 엔터키를 누르라는 안내 메시지 출력
  printf("10초가 되면 엔터키를 누르세요");

  while (1)
  {
    //사용자로부터 입력을 받고, 입력하면 반복문 종료
    if (getchar())
      break;
  }

  //프로그램이 종료된다는 메시지 출력
  printf("종료되었습니다.\n");
  end = time(NULL);

  //경과된 시간 출력
  printf("경과된 시간은 %ld 초입니다. \n", end - start);
  return 0;
}
```
# 나무 높이 측정
```c
#define _CRT_SECURE_NO_WARNINGS
#include <math.h>
#include <stdio.h>

int main(void)
{
  double height, distance, tree_height, degrees, radians;

  printf("나무와의 길이(단위는 미터): ");
  scanf("%lf", &distance);

  printf("측정자의 키(단위는 미터): ");
  scanf("%lf", &height);

  printf("각도(단위는 도): ");
  scanf("%lf", &degrees);

  //입력된 각도를 radians로 변환
  radians = degrees * (3.141592 / 180.0);

  //나무의 높이 계산
  tree_height = tan(radians) * distance + height;
  printf("나무의 높이(단위는 미터): %lf \n", tree_height);

  return 0;
}
```
# 삼각함수 그리기
```c
#include <stdio.h>
#include <math.h>
#define PI 3.141592

//각도를 radians로 변환하는 함수
double rad(double degree)
{
  return PI * degree / 180.0;
}

//막대 그래프를 그리는 함수
void drawbar(int height)
{
  //주어진 높이만큼 *을 출력하여 막대 그래프 그리기
  for (int i = 0; i < height; i++)
    printf("*");
  printf("\n");
}

int main(void)
{
  int degree, x, y;

  //10도부터 170도까지 20도 간격으로 반복
  for (degree = 10; degree <= 170; degree += 20) 
  {
    //주어진 각도에 대응하는 y좌표 계산
    y = (int)(60 * sin(rad((double)degree)) + 0.5);

    //막대 그래프 그리기
    drawbar(y);
  }

  return 0;
}
```
# 공학용 계산기 프로그램 작성
```c
#include<stdio.h>
#include<math.h>

int menu(void)
{
  int n;
  printf("1.팩토리얼\n");
  printf("2.싸인\n");
  printf("3.로그(base 10)\n");
  printf("4.제곱근\n");
  printf("5.순열(nPr)\n");
  printf("6.조합(nCr)\n");
  printf("7.종료\n");
  printf("선택해주세요: ");
  scanf("%d", &n);
  return n;
}

void factorial()
{
  long long n, result=1, i;
  printf("정수를 입력하시오: ");
  scanf("%lld", &n);

  //팩토리얼 계산
  for (i = 1; i <= n; i++) 
    result = result * i;
  
  printf("결과 = %lld\n\n", result);
}

void sine()
{
  double a, result;
  printf("각도를 입력하시오: ");
  scanf("%lf", &a);

  //주어진 각도에 대한 sin 값 계산
  result = sin(a);
  
  printf("결과 = %lf\n\n", result);
}

void logBase10()
{
  double a, result;
  printf("실수값을 입력하시오: ");
  scanf("%lf", &a);

  //주어진 실수값에 대한 로그 (base 10) 계산
  if (a <= 0.0) 
    printf("오류\n");
  else
  {
    result = log10(a);
    printf("결과 = %lf\n\n", result);
  }
}

int main(void)
{
  while (1) {
    switch (menu()) {
    case 1:
      factorial();
      break;
    case 2:
      sine();
      break;
    case 3:
      logBase10();
      break;
    case 7:
      printf("종료합니다.\n");
      return 0;
    default:
      printf("잘못된 선택입니다.\n");
      break;
    }
  }
}
```
