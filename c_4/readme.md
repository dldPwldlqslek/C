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
