::: quote
`$` 作为 `jQuery` 的选择器，承载了一代前端的太多记忆，但是你可能没有想到的是，在我们使用 `Dev Tools` 进行调试的时候， `$` 也有大放异彩的一天呢？
:::

### 1. `$0` 

在 `Chrome` 的 `Elements` 面板中， `$0` 是对我们当前选中的 `html` 节点的引用。

理所当然， `$1` 是对上一次我们选择的节点的引用， `$2` 是对在那之前选择的节点的引用，等等。一直到 `$4` 

你可以尝试一些相关操作(例如: `$1.appendChild($0)` )

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/about%2401.gif)

### 2. `$` 和 `$$` 

如果你没有在 `App` 中定义过 `$` 变量 (例如 `jQuery` )的话，它在 `console` 中就是对这一大串函数 `document.querySelector` 的别名。

如果是 `$$` 就更加厉害了，不仅仅是双倍的快乐，还能节省更多的时间，因为它不仅执行 `document.QuerySelectorAll` 并且它返回的是：一个节点的 **数组** ，而不是一个 `Node list` 。

虽然从本质上来说 `Array.from(document.querySelectorAll('div')) === $$('div')` :

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/docQueryAll.gif)

但是 `document.querySelectorAll('div')` 和 `$$('div')` 哪一种方式更加优雅呢？

### 3. `$_` 

调试的过程中，经常会打印一些变量的值，但如果你想看一下上次执行的结果呢？再输一遍表达式吗？ 

`$_` 登场， `$_` 是对上次执行的结果的 **引用** ：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/math_random.png)

### 4. `$i` 

现在的前端开发过程，离不开各种 `npm` 插件，但你可能没有想过，有一天我们竟然可以在 `Dev Tools` 里面来使用 `npm` 插件！

想玩玩新出的 `npm` 包，或者试试包的新特性？

还在建一个项目测试？你已经 `out` 了，有了Chrome 插件: Console Importer 以后，你只需要一个浏览器就可以畅玩所有 npm 包！

* 安装 `Console Importer` 插件，先打开这个[不存在的网址](https://chrome.google.com/webstore/category/extensions):

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/install_Console_Importer.gif)

* 运行 `$i('dayjs')` 几秒钟后，你就可以畅玩 `dayjs` 了:

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/dayjs-demo.gif)
