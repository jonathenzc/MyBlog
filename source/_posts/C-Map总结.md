title: C++ Map总结
date: 2015-03-03 12:10:59
categories: 【C++】
tags: [C++,map]
---
## C++ Map的一些总结 ##

---
最近在弄实验室的频繁子图挖掘的研究，需要对一些文本进行处理。在处理的过程中会使用到C++的map。

之前每次用C++的STL中的东西都会上网查其他人的博客，现在自己有博客了，可以将一些使用方法记下来，以后就可以看自己的博客了！

---

### map的创建 ###

---
创建map的时候需要指明键值对的类型，都可以使用自己声明的类型。

```C++
map<int,string> m; //这样声明的map是以int为键，string为值的变量
struct teamInfo
{
	string memberName;
	string position;
};
map<string,vector<teamInfo>> m; //那么这样的map是以string为键，teamInfo类型的vector为值的变量，其中teamInfo为刚刚自定义的结构体。
```

---

### map的插入 ###

---
map的插入可以使用它的`insert`方法和`map::value_type`来进行插入。

```C++
map<int,string> m;
m.insert(map<int,string>::value_type(1423,"string"));
m.insert(map<int,string>::value_type(3421,"string"));
```

---

### map的查找 ###

---
map的查找可以使用它的`find`函数来进行查找，获取map的值可以直接用`map[key]`来读取值

```C++
if(m.find(123) != m.end())
{
	cout<<"You find it!";
}
string s = m[123]; //直接使用[]来获取值
```

---

### map的遍历 ###

---
使用迭代器`iter`来进行遍历。

```C++
map<int,string> m
map<int,string>::iterator iter;
for(iter = m.begin();iter!=m.end();iter++)
{
	cout<<iter->first<<" "<<iter->second<<endl;
}
```