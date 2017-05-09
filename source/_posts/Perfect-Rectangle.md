title: Perfect Rectangle
date: 2016-08-30 14:58:27
categories: 【LeetCode】
tags: [LeetCode, Contest]
---
## {{ title }} ##

---

这道题目和室友讨论过，可以先判断是否存在矩形之间的覆盖，再求所有小矩形的面积之和是否等于大矩形的面积。

那么大矩形的坐标可以通过该点的坐标和（x+y）是否是最小和是否是最大，以O(n)的速度来找出。在找最左下坐标和最右上坐标时就可以把所有的矩形面积求和。 这样我们就以O(n)的速度来判断小矩形面积之和是否等于大矩形的面积。

那整个判断的瓶颈在于如何来判断矩阵之间是否是覆盖的。最简单的做法就是两两比较，那么这样的复杂度是O(n^2)的。室友实现后提交发现超时。

看了别人的discuss，发现可以这样来实现这道题目：

1. 判断所有小矩形的面积之和是否等于大矩形的面积
2. 小矩形中的点需满足以下三种情况：1. 属于大矩形顶点的点只会属于1个小矩形；2. 属于大矩形边的点只会属于2个小矩形；3. 属于大矩形内部的点只会属于2个或者4个小矩形。

这样我们可以根据上面提到的方法，先以O(n)的速度判断面积是否符合条件，接着定义3个map分别来记录点在顶点、边和内部的小矩形个数。最终在遍历这3个map如果不合适上面第2条的规则，那么我们就return false。整个方法的复杂度是O(n)的。

```C++
unordered_map<string, int> vertexMap;
unordered_map<string, int> edgeMap;
unordered_map<string, int> insideMap;

//返回小矩形各个顶点的位置,recV为大矩形的坐标
void getRecVertexPos(int x, int y, vector<int> recV)
{
	int cnt = 0;
	if (x == recV[0] || x == recV[2])
		cnt++;

	if (y == recV[1] || y == recV[3])
		cnt++;

	string s = to_string(x) + " " + to_string(y);
	if (cnt == 0) //INSIDE
		insideMap[s]++;
	else if (cnt == 1) //EDGE
		edgeMap[s]++;
	else if (cnt == 2) //VERTEX
		vertexMap[s]++;
}

//计算矩形面积
int area(vector<int> v)
{	
	return (v[2]-v[0])*(v[3]-v[1]);
}

//获取大矩形的坐标
vector<int> getRectBoarderPos(vector<vector<int>> rectangles, int &sumSquare)
{
	int minBoarder = INT_MAX, maxBoarder = INT_MIN;
	int minX, minY, maxX, maxY;
	vector<int> v;

	for (auto rec : rectangles)
	{
		if (rec[0] + rec[1] < minBoarder)
		{
			minBoarder = rec[0] + rec[1];
			minX = rec[0];
			minY = rec[1];
		}

		if (rec[2] + rec[3] > maxBoarder)
		{
			maxBoarder = rec[2] + rec[3];
			maxX = rec[2];
			maxY = rec[3];
		}

		sumSquare += area(rec);
	}

	v.push_back(minX);
	v.push_back(minY);
	v.push_back(maxX);
	v.push_back(maxY);

	return v;
}

bool isRectangleCover(vector<vector<int>>& rectangles) {
	if (rectangles.size() <= 1)
		return true;

	//先根据所有小矩形面积之和是否等于大矩形面积来筛选
	//获取大矩形的左下和右上坐标
	int sumSquare = 0;
	vector<int> outerRect = getRectBoarderPos(rectangles,sumSquare);

	if (area(outerRect) != sumSquare)
		return false;

	//再根据（1）在大矩形的顶角的点只属于1个小矩形，（2）在大矩形的边上的点属于2个矩形，（3）在大矩形的内部的点属于2个或者4个矩形
	for (auto rec : rectangles)
	{
		//左下
		getRecVertexPos(rec[0],rec[1],outerRect);

		//左上
		getRecVertexPos(rec[0], rec[3], outerRect);

		//右下
		getRecVertexPos(rec[2], rec[1], outerRect);

		//右上
		getRecVertexPos(rec[2], rec[3], outerRect);
	}

	//遍历3个记录顶点位置的map
	//vertex
	for (auto iter = vertexMap.begin(); iter != vertexMap.end(); iter++)
	{
		if (iter->second != 1)
			return false;
	}

	//edge
	for (auto iter = edgeMap.begin(); iter != edgeMap.end(); iter++)
	{
		if (iter->second != 2)
			return false;
	}

	//inside
	for (auto iter = insideMap.begin(); iter != insideMap.end(); iter++)
	{
		if (iter->second != 2 && iter->second != 4)
			return false;
	}

	return true;
}
```