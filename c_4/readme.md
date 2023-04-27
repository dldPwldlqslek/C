# dnffkffk
```c
#include <stdio.h>

int main(void)
{
  int x, y;
  int sum, diff, mul, div;

  x=20, y=10;
  
  sum = x+y;
  diff = x-y;
  mul = x*y;
  div = x/y;

  printf("두 수의 합: %d\n", sum);
  printf("두 수의 차: %d\n", diff);
  printf("두 수의 곱: %d\n", mul);
  printf("두 수의 몫: %d\n", div);
  
  return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
  int x, y, sum;
  
  printf("첫번째 숫자를 입력하시오:");
  scanf("%d", &x);
  
  printf("두번째 숫자를 입력하시오:");
  scanf("%d", &y);
  
  sum=x+y;
  printf("두수의 합: %d\n", sum);
  
  return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
  float radius, area;

  printf("반지름을 입력하시오: ");
  scanf("%f", &radius);

  area=3.14*radius*radius;
  printf("원의 면적:%f\n", area);
  
  return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
  double rate, usd;
  int krw;

  printf("환율을 입력하시오: ");
  scanf("%lf", &rate);

  printf("원화 금액을 입력하시오: ");
  scanf("%d", &krw);

  usd=krw/rate;
  printf("원화 %d원은 %lf달러입니다.", krw, usd);
  
  return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
  int id, pass;

  printf("아이디와 패스원드르 4개의 숫자로 입력하세요: ");

  printf("id: ____\b\b\b\b");
  scanf("%d", &id);

  printf("pass: ____\b\b\b\b");
  scanf("%d", &pass);

  printf("\a입력된 아이디는 \"%d\"이고 패스워드는 \"%d\"입니다.", id, pass);
  
  return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
  int x=10, y=10;

  printf("x=%d\n", x);
  printf("++x의 값=%d\n", ++x);
  printf("x=%d\n\n", x);

  printf("y=%d\n", y);
  printf("y++의 값=%d\n", y++);
  printf("y=%d\n", y);

  return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
  int x=10, y=10, z=33;

  x+=1;
  y*=2;
  x%=10+20;

  printf("x=%d y=%d z=%d\n", x, y, z);
  
  return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
  int x, y;

  printf("두개의 정수를 입력하시오: ");
  scanf("%d %d", &x, &y);

  printf("%d && %d의 결과값: %d\n", x, y, x && y);
  printf("%d || %d의 결과값: %d\n", x, y, x || y);
  printf("!%d의 결과값: %d\n", x, !x);
  
  return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
  int month, days;

  printf("달을 입력하시오: ");
  scanf("%d", &month);

  switch(month)
  {
    case 2:
          days = 28;
          break;
    case 4:
    case 6:
    case 9:
    case 11:
          days = 30;
          break;
    default:
          days = 31;
          break;
  }
    
  printf("%d월의 일수는 %d입니다.\n", month, days);
  
  return 0;
}
```
```c
#include <stdio.h>

int main(void)
{
  int x, y;

  for(y = 0;y < 5; y++)
  {
    for(x = 0;x < 10; x++)
        printf("*");
    printf("\n");
  }

  return 0;
}
```
