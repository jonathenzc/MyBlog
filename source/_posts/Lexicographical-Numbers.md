title: Lexicographical Numbers
date: 2016-08-25 18:21:59
categories: 【LeetCode】
tags: [LeetCode]
---
## {{ title }} ##

---

这道题目用递归来做,"10"<"100"

```C++
void helper(int start, int end, vector<int> &v)
{
	if (start <= end)
	{
		v.push_back(start);
		helper(start*10, end, v);
		if (start+1 <= (start / 10) * 10 + 9)
			helper(start+1,end,v);
	}
}

vector<int> lexicalOrder(int n) {
	vector<int> v;

	helper(1, n, v);

	return v;
}
```