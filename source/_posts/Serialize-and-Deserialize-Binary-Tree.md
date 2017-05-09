title: Serialize and Deserialize Binary Tree
date: 2016-10-17 11:32:46
categories: 【LeetCode】
tags: [LeetCode, Tree, Design]
---
## {{ title }} ##

---

一开始没看清题目，实际上不用它那套层遍历也可以完成的，测试样例是“codec.deserialize(codec.serialize(root))”的风格。看了discuss，发现很多人都是用前序遍历来实现的，所以效率很高。

层遍历的序列化比较简单，用一个队列来储存节点，每个节点的null也塞入队列，在最后的时候把结尾无用的null去掉就可以了。

反序列化可以利用下标来实现，先用个容器存一下节点，如果根节点的下标是i，那么满二叉树下的左、右儿子下标为2\*(i+1)-1和2\*(i+1)。但题目的二叉树不一定是满二叉树。 经观察，下标还需要减去之前null的个数，即左、右儿子的下标为2\*(i+1-nullCnt)-1和2\*(i+1-nullCnt)。

