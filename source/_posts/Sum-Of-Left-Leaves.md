title: Sum Of Left Leaves
date: 2016-09-29 22:13:39
categories: 【LeetCode】
tags: [LeetCode, Tree]
---
## {{ title }} ##

---

```C++
	int helper(TreeNode *node, bool isFromLeft)
	{
		if (node != NULL)
		{
			if (isFromLeft && node->left == NULL && node->right == NULL)
					return node->val;
			else
				return helper(node->left, true) + helper(node->right, false);
		}
		else
			return 0;
	}
```