title: Sudoku Solver
date: 2016-06-01 19:07:14
categories: 【LeetCode】
tags: [LeetCode, Hash Table, Backtracking]
---
## {{ title }} ##

---

问题是求解一个数独，数独肯定有唯一解。

判断一个数独合法可以用[http://jonathenzc.github.io/2015/05/31/Valid-Sudoku/](http://jonathenzc.github.io/2015/05/31/Valid-Sudoku/ "Valid Sudoku")来求解

先构造出3个储存行、列、九宫格所用数字的数组。

利用递归，传入3个数组、数独结构、当前遍历的位置（i,j）

```
    	if (i_val == 9)  //数独全部遍历完
    		return true;
    	
    	if (j_val == 9) //列到头了，换下一行填写
    		return sudokuHelper(board,rowmap,colmap,blockmap,i_val+1,0);
    
    	if (board[i_val][j_val] != '.')换下一列
    	{
    		return sudokuHelper(board, rowmap, colmap, blockmap, i_val, j_val+1);
    	}
    	else
    	{
    		for (int i = 1; i <= 9; i++)
    		{
    			int binaryBit = 1 << i;
    			if ((rowmap[i_val] & binaryBit) == 0 && (colmap[j_val] & binaryBit) == 0 &&
    				(blockmap[i_val / 3 * 3 + j_val / 3] & binaryBit) == 0)
    			{
    				board[i_val][j_val] = i + '0';
    				rowmap[i_val] |= binaryBit;
    				colmap[j_val] |= binaryBit;
    				blockmap[i_val / 3 * 3 + j_val / 3] |= binaryBit;
    
    				if (!sudokuHelper(board, rowmap, colmap, blockmap, i_val , j_val + 1))
    				{
    					rowmap[i_val] -= binaryBit;
    					colmap[j_val] -= binaryBit;
    					blockmap[i_val / 3 * 3 + j_val / 3] -= binaryBit;
    					board[i_val][j_val] = '.';
    				}
    				else
    					return true;
    			}
    		}
    	}
    
    	return false;
```  