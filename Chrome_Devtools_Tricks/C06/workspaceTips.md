::: quote
我们总是习惯于先在 `IDE` 或者文本编辑器中修改代码，然后再进入 `Chorme` 中进行调试，那有没有想过直接就在 `Chrome` 中来修改我们的代码呢？
:::

### 1. 在 `Chrome` 中修改你的文件

代码执行的位置也是最容易编辑代码的位置。如果把项目的文件夹直接拖到 `Source` 面板， `DevTools` 会将修改同步到系统文件中。

这对于快速修复代码非常方便：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C06/work_space_01.gif)

### 2. `Workspace` 支持即时同步样式

正如我们刚才所说，一旦设置好了 `DevTools workspace` ，就可以在 `Sources` 面板中编辑 `HTML` 和 `JavaScript` （或者甚至是 `TypeScript` ，如果你有 `sourcemaps` ）文件，按 `ctrl + s` 后它将被保存 在文件系统中。

但是在样式方面它提供了更好的支持。 因为即使你只是在 *“元素”* 面板的 *“样式”* 部分中编辑样式规则，它也会立即同步。
请注意，是立刻！

![](https://wingman-1300536089.file.myqcloud.com//chrome/C06/work_space_02.gif)

**"黑魔法!"**

### 3. 为新选择器选择目标位置

向现有选择器添加新样式

* 按下 `+` 号，添加新样式：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C06/work_space_03.gif)

:::tip 敲黑板
设置 `Workspace` 后，浏览器中所做的更改不仅会持久的保存到文件系统中，而且， `CSS` 的更改保存在文件系统后，立即就被浏览器选中并显示在你的页面上。**这一过程不需要刷新。**

我们 `没有使用额外的工具` - 没有 `webpack` 的热更新模块或者其他东西 - 只有一个本地服务以及 `DevTools' workspace` 而已。
:::

### 5. XHR/fetch 断点

在某一特定时刻，你想要对已发送的 `“ajax”` 请求进行捕获怎么做呢？
可以使用 `XHR/fetch breakpoint` 。

你可以添加部分 `URL` 作为触发器或监听任何请求：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C06/add_new_request_breakpoint.png)
