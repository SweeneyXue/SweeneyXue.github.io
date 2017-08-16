---
title: Fibonacci算法
date: 2016-11-23 20:12:48
tags: 算法
categories: coding
---

[POJ1000](http://poj.org/problem?id=1000)

**计算Fibonacci数列**
Fibonacci数列又称斐波那契数列，又称黄金分割数数列，指的是这样一个数列：1、1、2、3、5、8、13、21。
<!--more-->
```c
//c语言迭代法
#include<stdio.h>
int main()
{
	int t1=0,t2=1,display=0,t=1,n;
	scanf("%d",&n);
	printf("%d\n%d\n",t1,t2);
	display=t1+t2;
	while(t<(n-1))
	{
		print("%d\n",display);
		t1=t2;
		t2=display;
		display=t1+t2;
		t++;
    }
    return 0;
}
```
“通项公式法”

```c
/C语言通项公式
#include<stdio.h>
#include<math.h>
int fib(int n)
{
	double a=(1+sqrt(5))/2;
	double b=(1-sqrt(5))/2;
	double c=sqrt(5)/5;
	double v1=0;
	int v2=0;
	if(n>0)
	{
		for(int i=0;i<n;i++)
		{
			v1=c*(pow(a,i)-pow(b,i));
			v2=(int)v1;
			printf("%d\n",v2);
		}
		return 0;
	}
	else
	{
		return -1;
	}
}
int main()
{
	int n;
	scanf("%d",&n);
	fib(n);
	return 0;
}
```
