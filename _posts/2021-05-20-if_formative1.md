---
layout: single
title: "수행평가 "
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"
cateogries: "형성평가"
---

### 01. 사주보기
![saju](/assets/images/saju.jpg)
~~~c
#include <stdio.h> 
int main(void) 
{ int year,month,day,result; 
  
 printf("당신의 사주를 봐드립니다.\n"); 
 printf("연도 월 일을 차례대로 입력하세요 : "); 
 scanf("%d,%d,%d",&year,&month,&day); 
  
 result=(year-month+day)%10; 
 if(result==0) 
 printf("당신의 사주는 대박입니다.\n");
 else 
 printf("당신의 사주는 그럭저럭입니다.\n"); 
 return 0; 
 }
 ~~~ 
 
 
### 02. 3개의 터널 통과
![tunnel](/assets/images/tunnel.jpg)
~~~c
#include <stdio.h>
int main(void)
{ int tunnul_1, tunnul_2, tunnul_3;
printf("세 터널의 높이를 차례대로 입력하세요 : ");
scanf("%d,%d,%d",&tunnul_1,&tunnul_2,&tunnul_3);
if(tunnul_1<=170)
printf("충돌 %d", tunnul_1);
else if(tunnul_2<=170)
printf("충돌 %d", tunnul_2);
else if(tunnul_3<=170)
printf("충돌 %d", tunnul_3);
else
printf("무사 통과");
return 0;
}
~~~

### 03. 이 달은 며칠까지 있을까?
![month](/assets/images/month.jpg)
~~~c
#include <stdio.h>
int main(void)
{ int year, month;
printf("연도와 월을 입력하세요 : ");
scanf("%d%d", &year, &month);
printf("%d년 %d월의 마지막날은 ", year, month);
if(month==1||month==3||month==5||month==7||month==8||month==10||month==12)
printf("31일");
else if(month==4||month==6||month==9||month==11)
printf("30일");
else
{
if((year%4==0 && year%100!=0) || year%400==0)
printf("29일");
else
printf("28일");
}
printf("입니다.\n");
return 0;
}
~~~

### 04. 30분 전 
![clock](/assets/images/clock.PNG)
~~~c
#include <stdio.h>
int main()
{
 int hour, min;
 printf("시간과 분을 입력하세요 : ");
 scanf("%d %d", &hour, &min);
 printf("입력과 시간의 30분 전 시간은 ");
 if(min>=30)
 printf("%d시 %d분\n", hour, min-30);
 else
 {
 if(hour==0)
 printf("%d시 %d분\n", 23, min+30);
 else
 printf("%d시 %d분\n", hour-1, min+30);
 }
 return 0;
}
~~~

### 05. 용돈으로 책을 구입할 수 있는지 판단하는 프로그램
![error](/assets/images/error.PNG)
~~~c
#include <stdio.h>
 int main()
{
 int money, remain, book = 15000;
 printf("책의 가격은 15000원입니다.\n");
 printf("당신이 가진 용돈은 얼마인가요?: ");
 scanf("%d", &money);
 if(money>=book){
 remain=money-book;
 printf("책을 구입하였습니다. 이제 남은 용돈은 %d입니다.\n", remain);}
 else
 printf("책을 구입하지 못했습니다.");
 return 0;
}
~~~

### 06. 도어락
![doorlock](/assets/images/doorlock.PNG)
~~~c
#include <stdio.h>
 int main()
{
 int select;
 char dic='c', ic;
 int dpw=24680, pw;
 double dfig=1.2345678, fig;
 printf("장치 선택: ");
 scanf("%d", &select);
 if(select==1)
   {
    printf("IC카드: ");
    scanf(" %c", &ic);
   }
   else if(select==2)
   {
    printf("비밀번호: ");
    scanf("%d", &pw);
   }
   else
   {
    printf("지문: ");
    scanf("%lf", &fig);
   }
   if (dic==ic || dpw==pw || dfig==fig)
     printf("문 열림~");
   else
     printf("디리릭!디리릭!");
  
   return 0;
}
~~~

### 07. 가위바위보
![play](/assets/images/play.PNG)
~~~c
#include <stdio.h>
 
int main()
{
 char com, user;
 com='s';
 printf("r/s/p: ");
 scanf("%c", &user);
 if(com==user)
 printf("비겼다");
 else if((com=='r'&&user=='p') || (com=='p'&&user=='s') || (com=='s'&&user=='r'))
 printf("이겼다");
 else
 printf("졌다");
 return 0;
}
~~~

### 08. 성적 계산
![grade](/assets/images/grade.PNG)
~~~c
#include <stdio.h>
main()
{
 float a, b, c;
 int d, e, f;
 float score;
 printf("*** 과목별 점수 계산 프로그램 ***\n");
 printf("중간고사 반영비율/받은 점수를 입력하세요 : ");
 scanf("%lf %d", &a, &d);
 printf("기말고사 반영비율/받은 점수를 입력하세요 : ");
 scanf("%lf %d", &b, &e);
 printf("수행평가 반영비율/받은 점수를 입력하세요 : ");
 scanf("%lf %d", &c, &f);
 score = (a*d)+(b*e)+(c*f);
 printf("점수는 % .1f 입니다.\n", score);
}
~~~

### 09. 좌표 평면
![math](/assets/images/math.jpg)
~~~c
#include <stdio.h>

int main() 
{
  float x, y;
  printf("(x, y) : ");
  scanf("(%f, %f)", &x, &y);
  if(x>0 && y>0)
  printf("1사분면");
  else if(x<0 && y>0)
  printf("2사분면");
  else if(x<0 && y<0)
  printf("3사분면");
  else if(x>0 && y<0)
  printf("4사분면");
  else if(x==0 && y==0)
  printf("원점");
  else
  printf("정의할 수 없습니다.");
}
~~~
