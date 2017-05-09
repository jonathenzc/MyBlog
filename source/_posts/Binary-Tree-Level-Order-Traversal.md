title: Binary Tree Level Order Traversal
date: 2015-05-24 21:57:57
categories: 【LeetCode】
tags: [LeetCode, Tree, Breadth-first Search]
---
## {{ title }} ##

---

这道题目给定一颗二叉树，返回这棵树的“层序”遍历节点值。从最上层到最下层，从左到右访问。

比如一棵树是

<img src="/img/BinaryTreeLevelOrder.png"  class="img-shadow img-center"/>

那么结果返回[[3],[9,20],[15,7]]。

这道题目我利用广搜来做，使用队列来实现广搜。我定义这样的结构体，其中有树节点和该节点所在的层。队列的类型就是这个结构体的类型。

在大循环里进行广搜，当队列为空时循环结束。在循环中，

1. 首先处理每层元素的记录操作，弹出队列最上面的元素，如果该元素的层数和之前的一个元素的层数相同，那么就继续将该元素的值压入vector中；如果不同表明到了新的一层，那么将上一层的vector压入到大vector中并清空上一层的vector（因为我就用了一个小vector）；
2. 接着处理当前节点的左右子节点，如果不为空，就压入队列，并将层数加1；
3. 在循环外将最后一层的小vector压入大vector即可。