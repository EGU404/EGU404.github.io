---
layout: single
title: "조건문"
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"
categories: C언어수행
last_modified_at: 2021-06-18 T08:06:00-05:00
---

### 01. 사주보기  
![saju](/assets/images/sajubolae.jpg)  
~~~c  
#include <stdio.h>
main()
{
 int year, month, day, res;
 printf("당신의 사주를 봐드립니다.\n연도, 월, 일을 차례대로 입력하세요 : ");
 scanf("%d %d %d", &year, &month, &day);
 res= year-month+day;
 if (res%10==0)
  printf("당신의 사주는 대박입니다.\n");
 else
  printf("당신의 사주는 그럭저럭입니다.\n");
 
}
~~~

### 02. 3개의 터널 통과  
![tunnel](/assets/images/tunnel.jpg)  
~~~c  
#include <stdio.h>
main()
{ 
  int a, b, c;
  printf("세 터널의 높이를 차례대로 입력하세요 : ");
  scanf("%d %d %d", &a, &b, &c);
  if(a<= 170)  printf("충돌 %d", a);
  else if (b<=170) printf("충돌 %d", b);
  else if (c<=170) printf("충돌 %d", c);
  else
   printf("무사 통과");
}
~~~

### 03. 이 달은 며칠까지 있을까?
![calendar](/assets/images/day.jpg)  
~~~c  
#include <stdio.h>
 
int main(void)
{
 int year, month;
  printf("연도와 월을 입력하세요: ");
 scanf("%d %d", &year, &month);
 printf("%d년 %d월의 마지막 날은: ", year,month);
 
 if(month==1||month==3||month==5||month==7||month==8||month==10||month==12)
  printf("31");
 else if(month==4||month==6||month==9||month==11)
  printf("30");
 else
{
  if ((year%4==0 && year%100!=0) || year%400==0)
   printf("29");
 else;
  printf("28");
}
  printf("입니다 \n");
 return 0;
}
~~~


