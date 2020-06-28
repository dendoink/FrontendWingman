::: quote
说到 `Drawer` 大部分的朋友可能都很陌生，那 `Drawer` 是个什么东西？
:::

### 什么是 `Drawer` ？

`Chrome DevTools` 有很多部分，被分为9个 `tab` (俗称选项卡) ( `Elements` ， `Console` ， `Sources` ， `Network` ， 等等...)
但是，那仅仅是它的一部分而已！有一组平行的选项卡，被隐藏在主窗口之下。这个组合被称为 **`Drawer`**

### 1. 如何打开 `Drawer` ?

当你在 `DevTools` （任何选项卡）中时，按 `[esc]` 来显示它，再次按 `[esc]` 隐藏它：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C06/open_drawer.gif)

默认情况下，您会看到一个 `console` 选项卡。 与主面板的 `console` 完全相同。 这就是为什么主面板会显示除了 `console` 之外的每个主要标签（ `Elements` ， `Sources` ， `Network` ...）- 因为在主面板中显示 `console` 没有意义。

这样的 `console` 很方便，例如在 `Elements` 选项卡打开时，我们同时可以看到 `console` 面板。但是在 `Drawer` 中其实还隐藏了更多细节。

### 2. `Drawer` 里面到底有什么？

`Drawer` 里隐藏着许多其他功能，大多数时候你可能不需要用到它们，这也是它们为什么被隐藏起来的原因，然鹅，你可以直接选择你想展示在这里的功能。

点击主页面在 `Drawer` 的 `console` 面板前面的 `⋮` 图标来打开完整选项列表。另外，你也可以打开之前我们提到的 `command Menu` ，然后输入 `Drawer` 来打开

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C06/show_animation.gif)

所有的选项：

* `Animations` 
* `Changes` 
* `Console` 
* `Coverage` 
* `Network conditions` 
* `Performance monitor` 
* `Quick source` 
* `Remote devices` 
* `Rendering` 
* `Request blocking` 
* `Search` 
* `Sensors` 
* `What’s new` 
后面我们会介绍一些经常用到的：

### 3. `Sensors` 控制传感器

如果你正在你的应用中使用一些获取位置信息的 `API` 而且想要测试一下它，总不能开着车环绕世界吧，(其实也不是不行😉)。

`Sensors` 面板可以让你模拟特定的位置: 支持从预定义的位置中进行选择，添加自己的位置，或者手动键入纬度/经度。

可以通过 `navigator.geolocation.getCurrentPosition(console.table)` 打印你当前的位置信息：
![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C06/drawer_sensor01.gif)

:::tip 敲黑板
如果你还不知道为什么可以直接传入 `console.table` 建议你看看[这一节](https://www.frontendwingman.com/Chrome/C03/consoleTips.html)
:::

如果你的 `App` 使用加速计， `Sensors` 面板也可以模拟设备在 3D 空间中的位置！

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C06/drawer_sensor02.gif)
