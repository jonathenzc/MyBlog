title: VS Code 更改缩进
date: 2015-08-03 11:23:34
categories: 【工欲善其事必先利其器】
tags: [VS Code, Python]
---
## {{ title }} ##

---

在VS Code上编写python代码经常会出现这样的情况：有时候打开python文件使用缩进会导致直接以tab(\b)进行缩进，而编译的时候必须得用空格，那我就得手动调整空格和制表符，挺麻烦的。所以可以调整编辑器的默认缩进格式。

File->Preferences->User Settings，这时候会弹出两个编辑框，Default Setting和Setting.json。

在settings.json中添加：

```json
{
	// Controls the rendering size of tabs in characters. Accepted values: "auto", 2, 4, 6, etc. If set to "auto", the value will be guessed when a file is opened.
	"editor.tabSize": 4,//默认是auto的，我改成了4

	// Controls if the editor will insert spaces for tabs. Accepted values:  "auto", true, false. If set to "auto", the value will be guessed when a file is opened.
	"editor.insertSpaces": "auto",
}
```

将tabSize改成4，这样每次缩进都会是4个空格了