::: quote
我们看到的 `DevTools` 的功能，其实只是有限的表面部分，怎么去探索更多的功能呢？
:::

### 1. Command Menu

我们可以使用 `Command` 菜单，快速找到那些被隐藏起来的功能。它就相当于 `WebStorm` 中的 `Find Action` (查找动作) 或者 `Visual Studio Code` 中的 `Command Palette` ：

* 在 `Chrome` 的调试打开的情况下 按下 [ `Ctrl]` + `[Shift]` + `[P]` (Mac： `[⌘]` + `[Shift]` + `[P]` )
* 或者使用 `DevTools` 的 `dropdown` 按钮下的这个选项:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/dropdowm.png)

下图中，我整理了可供选择的命令列表，归为几个部分：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/cmd_menu_section.png)

> `Chrome DevTools` 竟然有那么多强大的功能!

### 2. 截屏的新姿势

当你只想对某一个 `DOM` 节点截图时，大概率会用工具弄半天，但现在不需要了：

直接选中那个节点，打开 `Command` 菜单并且使用 **节点截图** 的就可以了。

你以为这就是全部了吗？你还可以用这种方式 **全屏截图**  - 通过 `Capture full size screenshot` 命令。请注意，这里说的是全屏，并不是嵌入页面的一部分。

一般来说这可是得使用浏览器插件才能做到的事情！

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/capture.gif)

::: warning 注意
**节点截图有时会失效**，全屏截图如果页面内容过多的话，可能会截图不全，建议大家谨慎使用。
:::

### 3. 快速切换面板

`DevTools` 使用双面板布局，一般都是： `元素面板` + `资源面板` ，会自动根据屏幕可用的部分，将不同面板横向或纵向排列。

但我们在调试 PC 端的代码和手机端的代码时，习惯于用不同的布局方式。

怎么重置 `DevTools` 的布局呢？将 `样式面板` 从 `html预览` 的底部移动到右边或者周围其他的位置呢？

打开 `Commands` 菜单并且输入 `layout` (这里不再显示你已经激活的选项)：

* 使用横向面板布局
* 使用纵向面板布局
* 使用自动面板布局

试试看：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/layout.gif)

要达到这一效果，你还可以用 dock 相关的命令，输入 `dock to left` 或者 `dock to bottom` 试试：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/Dock-to-button.gif)

### 4. 快速切换主题

我们经常在电脑前一坐就是一天，你能忍受一直看着白闪闪的屏幕吗？

在 `Commands` 菜单中寻找与 `theme` 相关的选项，实现 `明亮` & `暗黑` 两种主题之间的切换：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/theme.gif)
