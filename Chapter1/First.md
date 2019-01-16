# [了解事件驱动](https://www.cnblogs.com/dxy1982/p/3791253.html)

​	前端JavaScript只干的两件事：操作[BOM](https://www.cnblogs.com/gaoya666/p/8560745.html)与操作DOM，那么什么时候去干这些事呢？答案是需要干的时候去干。那么什么时候是需要干的时候呢？答案是事件被触发的时候。这就是通常所说的“事件驱动开发”。

​	在事件被触发之前，所有的结构被静态的呈现出来，在事件触发滞后，动态的行为发生，重新产生新的静态结构，事件与状态构成了事件驱动开发的基本要素。

​	**事件的类型**

　　事件指由用户直接触发的行为，通常包括下列各种事件：

​	**鼠标事件**： 鼠标单击(click, mousedown, mousemove)，双击(dbclick)，滚轮事件(mousewheel)，鼠标移动(mousemove, mouseover, mouseout)。

​	**键盘事件**： 键按下，松开 (keydown, keypress, keyup)。

​	**上面的行为引发的事件**： 获得/失去焦点(focus, blur)，打开/关闭页面(load, unload)，选中文本(select)，修改文本内容(change)，窗口调整(resize)等。



**事件的响应 - 回调函数**

1. 静态绑定

　　这种做法是在书写HTML的时候就绑定好其回调函数，看个例子：

```html
<input type="button" value="Click Me" onclick="demo()"></input>
```

   2.动态绑定

```html
<input id="btnStart" type="button" value="Click Me"></input>
<script>
  var btnStart = document.getElementById('btnStart');
  btnStart.onclick = function() {
    alert('click event');
  };
</script>
```