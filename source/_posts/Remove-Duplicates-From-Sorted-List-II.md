title: Remove Duplicates From Sorted List II
date: 2015-06-03 18:27:09
categories: 【LeetCode】
tags: [LeetCode, Linked List]
---
## {{ title }} ##

---

给定一个有序列表，凡是列表中元素有相同的节点就要去掉，返回处理好的节点，比如1->2->3->3->4->4->5，那么返回1->2->5；又比如1->1->1->2->3，那么返回2->3。

我这里有两个函数，一个是题目要求返回的函数，还有一个函数的功能是忽略掉重复的元素，比如1->2->3->3->4，当我传入节点1，那么返回就是节点1，当我传入节点3，那么它将会忽视掉重复的元素，返回节点4，如果节点4的值变成3，那么就返回NULL。

有了这个函数的帮助，我们先找到第一个没有重复的节点(因为需要有个头节点)，接着对这个节点的下一个节点反复做这个忽视重读的函数，将那些没有重复的节点连在一起。

```C++
ListNode *ignoreDuplicate(ListNode *node)
{
	bool containsDuplicate = false;
	while (node != NULL && node->next != NULL)
	{
		if (node->val == node->next->val)
		{
			node = node->next;
			containsDuplicate = true;
		}
		else
		{
			if (containsDuplicate)
			{
				containsDuplicate = false;
				node = node->next;
			}
			break;
		}
	}
	if (containsDuplicate)
		node = node->next;
	return node;
}
ListNode* deleteDuplicates(ListNode* head) 
{
	if (head != NULL)
	{
		ListNode *headCopy = head;
		//没重复就返回当前指针，有重复就第一个不同的节点
		ListNode *headIter = ignoreDuplicate(head);
		while (headIter != NULL && headCopy->val != headIter->val)//开头有重复元素
		{
			headCopy = headIter;
			headIter = ignoreDuplicate(headIter);
		}
		//找出第一个单独元素，可以作为整个列表的头节点
		head = headIter;
		while (headIter != NULL && headIter->next!= NULL)
		{
			ListNode *headNext = headIter->next;
			ListNode *nextIter = ignoreDuplicate(headNext);
			headIter->next = nextIter;
			if (headNext!=NULL && nextIter != NULL && headNext->val == nextIter->val)
				headIter = headIter->next;
		}
	}
	return head;
}
```