
::: quote
除了基本的功能，还有哪些好用却不为人知的技巧？
:::

### 1. 插入样式规则的按钮

把鼠标悬停在样式选择器的最下面，会看到几个可以快速添加 `Color` 和 `Shadow` 属性的按钮：

* `text-shadow` 
* `box-shadow` 
* `color` 
* `background-color` 

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C05/element_addrule.gif)

### 2. 在元素面板中展开所有的子节点

一个一个点击 `▶` 展开太慢？右键选择 `expand recursively` ！：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C05/recursively.gif)

### 3. DOM 断点

有时脚本修改了 `DOM` ，但修改的是哪部分？什么时候修改的呢？

这样的情况下，你就可以添加一个 `DOM` 断点：监听节点被添加或者移除 / 属性被改变。

* 点击"..." 符号或者右击你想添加监听的元素

* `subtree modifications` : 监听任何它内部的节点被 `移除` 或者 `添加` 的事件

   

* `attribute modifications` : 监听任何当前选中的节点被 `添加` ， `移除` 或者 `被修改值` 的事件

   

* `node removal` : 监听被选中的元素被 `移除` 的事件

   
![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C05/dom_break.png)

页面重新加载时会记住断点。当你设置了一个或多个断点的时候，可能都忘了它们所标记的位置了。怎么找它们呢？：在 `Elements` 视图中有视觉提示，

有时你添加了断点的元素被隐藏在一些折叠起来的父级元素中，不要担心 - 他们会在 `Element` 中用高亮展示出来:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C05/dom_break_02.png)

`Sources` 中也有专用列表:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C05/dom_%20break_01.png)