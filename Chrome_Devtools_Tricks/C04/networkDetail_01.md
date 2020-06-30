::: quote
`Network` 和我们每天的工作息息相关，但是你真的了解它吗？
:::

### 1. 隐藏 network overview

`Network` 面板，通常我们不太关心时间轴的信息，那么 `Overview` 就可以隐藏起来啦！

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/close_over_view.gif)

### 2. Request initiator 显示调用堆栈信息

`Network` 面板中的 `initiator` 这一列告诉我们是脚本的哪一行触发了当前请求。（通常显示的是，调用堆栈中触发请求的那一步。）

如果你用的是一个本地化的 `fetch` API， 那它将会指向一些低层级的类库的代码 - 例如 当我们在 `Angular` 配合使用 `Axios` 或者 `zone.js` 的时候，这时指向的是 `xhr.js` 

除了这些外部库之外，如果你想看到代码的哪一部分触发了请求：

将鼠标悬停在显示的 `initiator` （例如 外部库）上，就可以看到完整的调用堆栈，包括文件：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/initiator.gif)

### 3. 自定义请求表

在请求表中，可以看到有关每个请求的几条信息，例如： `Status` ， `Type` ， `Initiator` ， `Size` 和 `Time` 。但是我们同样可以添加更多自己想看到的信息(例如 我经常添加 `Method` )。：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/custom_table_network.gif)

:::tip 敲黑板
`Network` 面板里展示出来那些信息，都可以添加到这里。
:::

要自定义显示哪些列，右键单击请求表标题上的任意位置。

:::warning 请注意
`Response Headers` 是一个有更多选项的完整的子菜单，你甚至可以定义选项！
:::

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/custom_Response_Headers.gif)
