title: Elimination Game
date: 2016-08-30 14:58:36
categories: 【LeetCode】
tags: [LeetCode, Contest]
---
## {{ title }} ##

---

我一开始想过模拟，但是一想到模拟中对vector的删除操作的复杂度，我就觉得不能单纯的用模拟来实现。

所以我的方法是用两个指针，一个指向头，一个指向尾，同时定义一个diff变量，表示每次删除操作的跳步距离。

根据观察，我们发现其实每次跳步的距离都是上一次跳步距离乘以2.


```C++
int lastRemaining(int n) {
	if (n == 1)
		return 1;

	int start = 1, end = n,diff=2;
	int numCnt = n;
	bool flag = true;

	while (numCnt != 1)
	{
		if (flag) //正向
		{ 
			flag = false;
			start = start + diff / 2;
			end = start + diff*(numCnt/2-1);
		}
		else //方向
		{
			flag = true;
			end = end - diff/2;
			start = end - diff*(numCnt / 2 - 1);
		}

		numCnt /= 2;
		diff *= 2;
	}

	return start;
}
```