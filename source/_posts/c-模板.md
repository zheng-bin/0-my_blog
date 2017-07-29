---
title: c++ 模板
date: 2014-12-24 21:12:16
tags:
  - C++
  - template
---

# 模板
* 模板定义形式
```
template<模板参数表>
类型名 函数名（参数表）
{
  函数体
}
```
* 模板参数表由逗号分隔开的参数构成，关键字：calss或typedef

## 函数模板

* 定义一个函数模板，获取数组元素最大值
```
<<<<<<< HEAD
#include <iostream>
#include <string>

template<typename T, int len>
T max(T array[len])
{
	t max = array[0];
	for(int i = 0; i < len; i++)
	{
		max = (max > array[i]) ? max:array[i];
	}
	return max;
}

int main()
{

	  int iarray1[5] = {5, 7, 8, 9, 2};
    int Max1 = max<int, 5>(iarray1);
    printf("%d\n",Max1);
    double iarray2[3]={1.23, 23.4, 12.2};
    double Max2 = max<double, 3>(iarray2);
    printf("%f\n",Max2);
    return 0;

}
```

=======



```




>>>>>>> 82c90aba39f2edb2496fc392c331600c27d7c9f8
## 类模板
