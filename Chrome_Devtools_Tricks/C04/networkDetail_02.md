::: quote
`Network` 还有哪些使用技巧呢？
:::

### 1. 重新发送 `XHR` 的请求

如何重新发送 `XHR` 的请求？还在刷新页面？

太老套了，试试这么做：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/replayxhr.png)

### 2. 禁止请求

当你想测试页面在某个接口失败时的表现，就可以使用 `Network` 面板中的禁止请求的方法。

有两种方式来禁用一个请求：

* 如果这个 `**请求已经在你的请求列表中**` ，你可以右键选择禁用来自当前 `URL` 的请求，或者来自当前域名的请求：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/block_request.png)

* 如果是在生产环境，或者你想使用一个正则规则来匹配一系列的请求进行禁用，就可以使用 `Drawer` 来禁用请求:

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/block_request_02.gif)

:::tip 敲黑板
如果你还不知道 `Drawer` 是什么，别担心，我们在后面的[章节](https://www.frontendwingman.com/Chrome/C06/drawerTips.html)会提到。
:::

### 3. 强制清除缓存刷新

在你没有打开 `devtools` 的情况下， `Chrome` 的刷新按钮只能简单的刷新当前页面，但是在你开启 `devtools` 的情况下，长按刷新按钮会多出两个选项：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C07/hardreload.gif)

* Hard Reload 强制刷新 
* Empty Cache and Hard Reload 清除缓存强制刷新

:::tip 敲黑板
你可以使用 `Ctrl` + `Shift` + `R` ( `Windows` ) 或 `Cmd` + `Shift` + `R` ( `Mac` ) 来强制刷新。
:::
