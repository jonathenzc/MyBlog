title: Find Minimum In Rotated Sorted Array
date: 2015-06-02 13:40:08
categories: 【LeetCode】
tags: [LeetCode, Array, Binary Search]
---
## {{ title }} ##

---

给定一个排序好的数组，这个数组会根据某个元素旋转，比如数组是0 1 2 3 4 5 6 7，经过旋转后得到4 5 6 7 0 1 2。问题是返回这个数组最小的元素。

当然扫一遍找最小元素是可以的，时间是`O(n)`，那么肯定是要比这个复杂度更低的，那么就是`O(logN)`，用二分来做。

我们发现当最右边的数大于最左边的数的时候，最左边的数就是最小的数，否则这个数列就不是顺序的了（当然问题里说没有重复的数）。

接着我们取下标为left+right一半的元素，如果这个数比右边的数要大，那表明最小的元素在右边；反之，最小元素在左边。

**更新后**

如果问题从最小值变成最大值我们该怎么改？当然我们可以把它归约到求出最小值的位置，然后前一个位置就是最大值。那么能不能直接在代码上进行修改呢？

```C++
	int findMax(vector<int>& nums) {
		int start = 0, end = nums.size() - 1;
		int maxCan = INT_MIN;
		while (start <= end)
		{
			int mid = start + (end - start) / 2;
			if (nums[mid] > nums[start])
				start = mid + 1;
			else if (nums[mid] < nums[start])
				end = mid;
			else
				start++;

			maxCan = max(maxCan,nums[mid]);
		}

		return maxCan;
	}
```