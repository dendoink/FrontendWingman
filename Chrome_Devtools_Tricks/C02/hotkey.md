::: quote
如果有人问你最有效提升开发效率的方式？你首先想到的肯定是快捷键！那在 Chrome 中有哪些值得我们去了解的快捷键呢？
:::

### 1. 切换 `DevTools` 窗口的展示布局

一般我在使用 `DevTools` 时， `dock` 的展示窗口都在底部 ，但是有时候我想把 `dock` 的窗口 切换到右边。

怎么做呢？

这时就可以通过 `DevTools` 的下拉菜单，或者命令菜单... 或者使用一个快捷键 `ctrl + shift + D` ( `⌘ + shift + D` Mac) 来实现位置的切换（通常是从 `开始的位置` 到 `右边位置` ，但如果一开始就是 `右边的位置` 那么会切换到 `左边的位置` ）:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/csd.gif)

### 2. 切换 `DevTools` 的面板

如果可以的话，我想成为一个不需要鼠标的开发者，日常开发中，我们常需要从 `元素面板` 跳转到 `资源面板` 并返回，这样往返的来调试我们的代码，怎么来节省鼠标点击的时间呢：

* 按下 `ctrl + [` 和 `ctrl + ]` 可以从当前面板向左/向右切换面板。

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/switch_tab.gif)

* 按下 `ctrl + 1` 到 `ctrl + 9` 可以直接转到编号 `1` ... `9` 的面板( `ctrl + 1` 转到元素面板， `ctrl + 4` 转到 网络信息面板等等)

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/cmd1-9.gif)

::: warning 请注意
第二组快捷键默认是禁用状态。你需要手动打开:
:::

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/settings.gif)

### 3. 递增/递减

接下来这个技巧，对调整样式是最有用的：通过使用 `带有` 或者 `不带有修饰键` 的 `上` / `下` 箭头按键， 你可以实现递增和递减 `0.1` ， `1` 或者 `10` 这样数值类型的值。

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/snippet-increase-decrease.png)

:::tip 敲黑板
这些操作对颜色同样生效！（虽然没什么用~）
:::

### 4. elements， logs， sources & network 中的查找

`DevTools` 中的前 `4` 个主要的面板，每一个都支持 `[ctrl] + [f]` 快捷查询，不同的面板查询条件有所区别：

* `Elements` 面板: 支持 `string` /选择器/ `XPath` 
* `Console` , `Network` , `Source` 面板: 字符串（区分大小写）

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/ctrl%2Bf.png)

:::tip 敲黑板
关于查询这个操作，其实不光是 Chrome 的调试工具中有, 几乎所有软件都有，快捷键也多是 `cmd` ( `ctrl` ) + `F` ，这里 `F` 就是 find 的意思，同理 `R` 是 refresh，所以刷新就是 `cmd` + `R` ，依次类推，理解以后你能够记住更多的操作，比如 `O` 代表 open。学习的过程中，尝试去理解设计者的出发点，往往能够收获更多。
:::

### 5. 所有快捷键

授人以鱼不如授人以渔，Chrome 里面所有的快捷键都可以在设置里找到：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/shortcut.gif)
