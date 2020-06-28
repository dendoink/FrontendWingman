::: quote
 你知道 `Network` 有哪些使用技巧吗？
:::

### 1. 隐藏 network overview

打开 `Network` 面板，你通常不太关心请求的时间轴信息
如果是这样，那么 `Overview` 的部分就可以隐藏起来啦！

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C04/close_over_view.gif)

### 2. Request initiator 显示调用堆栈信息

`Network` 面板中的 `initiator` 这一列告诉我们是脚本的哪一行触发了当期请求。（通常显示的是，调用堆栈中触发请求的那一步。）

但如果你用的是一个本地化的 `fetch` API， 那它将会指向一些低层级的类库的代码 - 例如 当我们在 `Angular` 配合使用 `Axios` 或者 `zone.js` 的时候，这时指向的是 `xhr.js` 

除了这些外部库之外，如果你想看到代码的哪一部分触发了请求：

将鼠标悬停在显示的 `initiator` （例如 外部库）上，你将看到完整的调用堆栈，包括你的文件：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C04/initiator.gif)

### 3. 自定义请求表

在请求表中，你可以看到有关每个请求的几条信息，例如： `Status` ， `Type` ， `Initiator` ， `Size` 和 `Time` 。但是你同样可以添加更多(例如 我经常添加 `Method` )。更多：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C04/custom_table_network.gif)

> 你可以添加所有 `Network` 面板里展示出来的信息。

要自定义显示哪些列，右键单击请求表标题上的任意位置。

> 请注意， `Response Headers` 是一个有更多选项的完整的子菜单，甚至可以定义你自己的选项。

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C04/custom_Response_Headers.gif)
