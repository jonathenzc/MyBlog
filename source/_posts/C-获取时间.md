title: C++获取时间
date: 2017-07-31 17:16:01
categories: 【C++】
tags: [C++]
---
## {{ title }} ##

---

```C++
#include<iostream>
#include<ctime>
using namespace std;
int main()
{
time_t now_time;
now_time = time(NULL);
cout<<now_time<<endl;

stringstream ss;
ss << now_time;
string timeStr;
ss >> timeStr;
cout << timeStr<<endl;
return 0;
}
```

参考资料：

1. [C++ 取得系统当前时间](http://www.cnblogs.com/Asa-Zhu/archive/2012/08/30/2664341.html)
2. [c/c++日期时间处理与字符串string转换](http://www.cnblogs.com/renjiashuo/p/6913668.html)