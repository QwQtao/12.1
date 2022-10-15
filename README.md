# 12.1
循环&amp;迭代（下）



//计算n的阶乘
循环的方法
int Fac1(int n)
{
	int i = 0;
	int ret = 1;
	for (i = 1; i <= n; i++)
	{
		ret *= i;
	}
	return ret;
}
int main()
{
	//求n的阶乘
	int n = 0;
	int ret = 0;
	scanf_s("%d", &n);
	ret = Fac1(n);//循环的方式
	printf("%d\n", ret);
	return 0;
}


递归的方法
int Fac1(int n)
{
	int i = 0;
	int ret = 1;
	for (i = 1; i <= n; i++)
	{
		ret *= i;
	}
	return ret;
}
int Fac2(int n)
{
	if (n <= 1)
		return 1;
	else
		return n* Fac2(n - 1);
}
int main()
{
	//求n的阶乘
	int n = 0;
	int ret = 0;
	scanf_s("%d", &n);
	ret = Fac1(n);//循环的方式
	printf("%d\n", ret);
	return 0;
}


//描述第n个斐波那契数
 递归的方法
int count = 0;
int Fib(int n)
{
	if (n == 3)
	{
		count++;
	}
	if (n <= 2)
		return 1;
	else
		return Fib(n - 1) + Fib(n - 2);
}
int main()
{
	int n = 0;
	int ret = 0;
	scanf_s("%d", &n);
	ret = Fib(n)
		; printf("ret=%d\n", count);
	return 0;
}
冗杂

迭代(循环)的方法
int Fib(int n)
{
	int a = 1;
	int b = 1;
	int c = 1;
	while (n > 2)
	{
		c = a + b;
		a = b;
		b = c;
		 n--;
	}
	return c;
}
int main()
{
	int n = 0;
	int ret = 0;
	scanf_s("%d", &n);
	ret = Fib(n)
		; printf("ret=%d\n", ret);
	return 0;
}
//效率
