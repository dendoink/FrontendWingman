::: quote
在调试的过程中，我们总要对 Dev Tools 里面的数据进行 复制 或者 保存 的操作，所以我们来看看，关于这些，有什么小技巧呢？
:::

### 1. `copy(...)` 

你可以通过全局的方法 `copy()` 在 `console` 里复制任何能拿到的资源（我们在后面还会提到这些资源）。例如 `copy($_)` 和 `copy($0)` 

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/copy&saving01.gif)

### 2. `Store as global` （存储为一个全局变量）

假如你在 `console` 中打印了一堆数据 (例如你在 `App` 中计算出来的一个数组) ，然后想对数据做额外的操作，比如刚刚说的 `copy` (在不影响它原来值的情况下) 。
那就可以将它转换成一个全局变量，只需要 **右击** 它，并选择 “ `Store as global variable` ”   (保存为全局变量) 选项。

第一次使用的话，它会创建一个名为 `temp1` 的变量，第二次创建 `temp2` ，以此类推。

使用这些变量来操作对应的数据，就不用担心会影响到原来的值了:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/copy&saving02.gif)

### 3. 保存堆栈信息( `Stack trace` )

大多数情况下，开发项目是一个团队协作，而**沟通的关键是，如何准确的描述问题** ， `console` 打印出来的堆栈的追踪信息，可以省去你和同事的很多沟通成本，我们可以直接把堆栈追踪信息保存为一个文件，而不只是发个截图给对方：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/save_log.gif)

### 4. 直接Copy HTML

相信大家都知道，右击或者点击在 `HTML` 元素边上的省略号 (...) 就可以将当前元素复制到剪贴板中:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/copy_01.gif)


但你不知道的是：古老的“CV大法”也可以!

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C02/copy_02.gif)
