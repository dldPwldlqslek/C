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
