::: quote
经常会发现，项目里面外部库的一大块 `JavaScript` ，或者选择器上的一些 `CSS` 规则，实际都没有用到，但是怎么找到并且优化这一部分内容呢？
:::

### 1. `coverage` 代码覆盖率 

`coverage` 可以提供冗余代码的细节信息。使用 `Drawer` 菜单或者 `Command` 菜单来打开它:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C06/drawer_coverage.gif)

`DevTools` 的 `coverage` 工具可以跟踪当前加载的 `JS` 和 `CSS` 文件的 `哪些行正在被执行` ，并显示 `未使用字节的百分比` , `绿色` 的线条表示 `已使用内容` ， `红` 线表示 `未使用的内容` :

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C06/drawer_coverage01.gif)

### 2. `Changes` 检查你修改的内容

在 Chrome 里调 `CSS` 应该是我工作的日常了，但我总是想将 `新写的样式` 与 `最初样式` 进行比较，看看到底有什么不一样，这时候就可以使用 `Drawer` 的 `Changes` ：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C06/drawer_changes01.gif)

### 3. 拿到 `source` 

与 `drawer console` 一样，当我要专注于 `Elements` 面板时，有时我也想看源代码，这时就可以在 `drawer` 中选择显示 `Source` 。

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C06/drawer_quicksource01.gif)

没有 `“主”Source` 面板的花里胡哨的功能，没有 `call stack` 或者 `control` ( `pause` ， `step over` ， 等等)按钮。但如果是 `快速查看代码` ，或者 `设置断点` ，它非常有用。

:::tip 敲黑板
触发的断点不会显示在 `Quick sources` 中，而是显示在主 `Source` 中。
:::

### 4. `Network conditions` 模拟网络状态

想测试页面资源的大小，或者测试应用的离线功能? 使用 `Drawer` 里的 `Network conditions` 面板模拟特定的网络行为：模拟互联网为典型的3G网络甚至离线！ 

除此之外， `Network conditions` 面板还可以自定义网络状态:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C06/drawer_network01.gif)
