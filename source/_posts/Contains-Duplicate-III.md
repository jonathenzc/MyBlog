title: Contains Duplicate III
date: 2015-06-02 13:01:23
categories: 【LeetCode】
tags: [LeetCode, Array, Hash Table]
---
## {{ title }} ##

---

这道题目算是[Contains Duplicate II](/2015/06/01/Contains-Duplicate-II/)的加强版，II的题目还是判断相等，而这道题目模糊了相等的概念，变成给定一个数t，判断数组中的数是否存在差值在这个t的范围内。

虽然Leetcode将这个问题的标签定为Binary Search Tree。我还是将它定为Hash Table。

我这里贴代码吧：

```C++
bool containsNearbyAlmostDuplicate(vector<int>& nums, int k, int t) 
{
	//键为vector中的元素，值为元素所对的下标
	map<int, int> m;
	for (int i = 0; i < nums.size(); i++)
	{
		auto it = m.lower_bound(nums[i] - t);
		if (it != m.end())
		{
			long long diff = it->first - nums[i];//用来处理溢出
			if (abs(diff) <= t)
			{
				int duplicateIndex = it->second;
				if (abs(duplicateIndex - i) <= k)
					return true;
			}
		}

		it = m.lower_bound(nums[i] + t);
		if (it != m.end())
		{
			long long diff = it->first - nums[i];//用来处理溢出
			if (abs(diff) <= t)
			{
				int duplicateIndex = it->second;
				if (abs(duplicateIndex - i) <= k)
					return true;
			}
		}
		m[nums[i]] = i;
	}
	return false;
}
```

主要的想法就是用到了`map`中的`lower_bound`，这个函数会返回输入数的下界，当然会有点不同，比如数组中有1,3,5,7,9，`lower_bound(3)`会返回3，而`lower_bound(4)`会返回5，不能算下界。

我的方法就是去找+t和-t在map中的下标，接着判断是否在k范围内。