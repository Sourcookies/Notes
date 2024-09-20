Event:用户交互时的操作

```
click
mousedown   按下鼠标触发
mouseup     松开
mousemove   移动时
mouseout    离开一定范围
load		页面内容加载完成时
blur 		失去焦点时
change		内容改变且失去焦点
focus 		获得焦点时
```

事件绑定：(注册事件处理程序)

三种方式：

```
1.设置标签的属性为事件处理程序
<input type="button" onmousemove="mouseMoveEvent()">

2.事件属性：事件处理函数
3.call addEventListener()
on + 事件 ：
	onclick or onfocus
	
addEventListener(事件类型名, 处理函数, boolean)	
```

JavaScript:

```
ECMAScript

DOM 文档对象模型

BOM(Brower) 浏览器对象模型

DOM: 操作HTML所有节点的入口 标签是元素节点 
```

```
document.getElementById("s").innerHTML = "123";
改变s内容

document.createElement();
document.createTextNode();
document.createAttribute();

element.appendChild();
element.insertBefore();
element.replaceChild();
element.removeChild();
```

