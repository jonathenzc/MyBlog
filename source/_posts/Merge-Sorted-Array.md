title: Merge Sorted Array
date: 2015-05-29 22:17:43
categories: 【LeetCode】
tags: [LeetCode, Two Pointers, Array]
---
## {{ title }} ##

---

给定两个排序好的容器nums1、nums2和这两个容器的大小m、n，问题是将容器nums2中的元素归并到nums1中，使得归并后的元素仍然是有序的。nums1的容器大小特别大，可以容纳m+n。

我一开始的思维被归并框死了，只想着弄个新的空间，用两个指针分别指向nums1和nums2,然后根据大小来插入。但实际上可以从后面开始来进行插入。

这次就直接上代码吧：

```C++
void merge(vector<int>& nums1, int m, vector<int>& nums2, int n) 
{
	int index = m + n - 1;
	int i = m - 1;//从nums1的最后开始访问
	int j = n - 1;//从nums2的最后开始访问

	//这里有个技巧，因为我们需要将nums2的元素移到nums1中，那么nums2中的元素肯定是要被移走的，所以循环的条件可以是j>=0
	//如果nums1的元素全没时（我是指m个元素）,nums2还有元素,接下来就只需要将nums2中的元素移到nums1,所以循环中的if判断需要加个i>=0来限制一下。
	while (j>=0)
	{
		if (i>=0 && nums1[i] > nums2[j])
			nums1[index--] = nums1[i--];
		else
			nums1[index--] = nums2[j--];
	}
}
```