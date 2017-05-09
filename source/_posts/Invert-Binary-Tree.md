title: Invert Binary Tree
date: 2015-06-15 15:47:00
categories: 【LeetCode】
tags: [LeetCode, Tree]
---
## {{ title }} ##

---

问题是翻转一颗二叉树，使得原树各个节点的左子树是原树的右子树。

比如原树是
```C++
     4
   /   \
  2     7
 / \   / \
1   3 6   9
```

翻转后是
```C++
     4
   /   \
  7     2
 / \   / \
9   6 3   1
```

这道题目可以用递归来做，也可以用迭代来做。

递归的话就是先将节点的左子树翻转，接着翻转右子树，最后交换该节点的左右子树。

```C++
//Recursion Version
TreeNode *invertTree(TreeNode *root)
	if(root!=NULL)
		invertTree(root->left); //翻转左子树
		invertTree(root->right); //翻转右子树
		//交换节点的左右子树
		TreeNode *temp = root->left;
		root->left = root->right;
		root->right = temp;
	return root;
```

迭代版本就是用栈来储存节点，先将根节点压入栈中，接着进入循环，当栈为空，那么这棵树也遍历好了。在循环开始的时候弹栈，当节点不为空时，压入该节点的左右子树，接着交换左右子树。

```C++
//Iteration Version
TreeNode *invertTree(TreeNode *root)
	stack<TreeNode*> s;
	s.push(root);
	while(!s.empty())
		TreeNode *fatherNode = s.top();
		s.pop();
		if(fatherNode!=NULL)
			s.push(fatherNode->left);
			s.push(fatherNode->right);
			//交换节点的左右子树
			TreeNode *temp = fatherNode->left;
			fatherNode->left = fatherNode->right;
			fatherNode->right = temp;
	return root;
```