---
open: true
---

## Chrome 的半壁江山

谷歌浏览器（通常简称为 `Chrome` ）由谷歌于 2008 年首次针对 `Microsoft Windows` 发布，后移植到 `Linux` ， `macOS` ， `iOS` 和 `Android` 。 

浏览器也是 `Chrome OS` 的主要组件，它可以作为 `Web` 应用的平台。[Chrome-维基百科](https://en.wikipedia.org/wiki/Google_Chrome)

浏览器的市场三足鼎立， `Chorme` ， `Safari` 和 `FireFox` ，从 2008 年 `Chrome` 横空出世以来，如今已经一家独大，占据半壁江山：

![](https://wingman-1300536089.file.myqcloud.com//chrome/BrowserUsageShare.png)

By <a href="//en.wikipedia.org/wiki/User: Efa" title="User: Efa">Efa</a> - OpenOffice Calc, <a href="https://creativecommons.org/licenses/by-sa/4.0/" title="Creative Commons Attribution-ShareAlike 4.0">CC BY-SA 4.0</a>, <a href="https://en.wikipedia.org/w/index.php?curid=60616332">Link</a>

对于大部分人来说， `Chrome` 可能只是个浏览器，但是对于开发人员来说，它更是一个强大无比的工具。

为了方便开发人员调试代码，主流的浏览器都内置了 `DevTools` ，无论你是前端还是后端，掌握 `Chrome` 的调试技巧意味着效率的直接提高。

这个系列要介绍的，就是 `Chrome-DevTools` 的使用技巧。

## DevTools 简介

> 本段内容引用于 [Chrome DevTools ](https://developers.google.com/web/tools/chrome-devtools/#_1) 。熟悉的同学可以跳过，也可以选择跳转到原链接访问，这里是为了给没有接触过 `chrome-devtools` 的同学科普一些基础概念。

### 打开 Chrome 开发者工具

* 在 `Chrome` 菜单中选择 `更多工具` → `开发者工具` 
* 在页面元素上右键点击，选择 `检查` 
* `Windows` : `Ctrl` + `Shift` + `I` 
* `Mac` : `Cmd` + `Opt` + `I` 

### 了解面板

我将从以下 8 个面板来讲述面板内容：

1. 元素面板
2. 控制台面板
3. 源代码面板
4. 网络面板
5. 性能面板
6. 内存面板
7. 应用面板
8. 安全面板

#### 1. 元素面板

使用元素面板可以自由操作 `DOM` 和 `CSS` 来迭代布局和设计页面。

* 检查和调整页面
* 编辑样式
* 编辑 `DOM` 

![](https://wingman-1300536089.file.myqcloud.com//chrome/elements.png)

#### 2. 控制台面板

在开发期间，可以使用控制台面板记录诊断信息，或者使用它作为 `shell` 在页面上与 `JavaScript` 交互。

* 使用控制台面板
* 命令行交互

![](https://wingman-1300536089.file.myqcloud.com//chrome/console.png)

#### 3. 源代码面板

在源代码面板中设置断点来调试 `JavaScript` ，或者通过 `Workspaces` （工作区）连接本地文件来使用开发者工具的实时编辑器

* 断点调试
* 调试混淆的代码
* 使用开发者工具的 `Workspaces` （工作区）进行持久化保存

![](https://wingman-1300536089.file.myqcloud.com//chrome/sources.png)

#### 4. 网络面板

使用网络面板了解请求和下载的资源文件并优化网页加载性能。

* 网络面板基础
* 了解资源时间轴
* 网络带宽限制

![](https://wingman-1300536089.file.myqcloud.com//chrome/network.png)

#### 5. 性能面板

* 记录和查看网站生命周期内发生的各种事件
* 提高页面的运行时性能。

![](https://wingman-1300536089.file.myqcloud.com//chrome/performance.png)

#### 6. 内存面板

* 跟踪内存泄漏。
* `JavaScript` CPU 分析器
* 内存堆区分析器

![](https://wingman-1300536089.file.myqcloud.com//chrome/memory.png)

#### 7. 应用面板

* 检查加载的所有资源
* `IndexedDB` 与 `Web SQL` 
* 本地和会话存储， `cookie` 
* 应用程序缓存，图像，字体和样式表

![](https://wingman-1300536089.file.myqcloud.com//chrome/application.png)

#### 8. 安全面板

* 证书问题
* 安全相关问题

![](https://wingman-1300536089.file.myqcloud.com//chrome/security.png)
