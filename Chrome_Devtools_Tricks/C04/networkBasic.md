::: quote
`Network` 作为调试中比不可少的一环，但你对它的了解有多少呢？
:::

打开 `Network` 的第一印象，满屏都是请求:

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/network-overview.png)

上面的截图，好像没有缺少任何有效信息，但是你只看到了自己想看到的，有很多的关键信息在不起眼的位置：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/DOM_LOAD_Time.png)

为什么大部分时候没有注意到呢？因为 DOM 结构渲染的时间，和执行 load 脚本的耗时，是在已经完成功能的情况下进行性能优化的时候才会用到。

日常工作的核心，只是通过这个面板上的过滤器，找到那些我们需要的请求，然后查看它的详细信息，判断它是否正确得返回了我们需要的值。

:::tip 敲黑板
如果细心的话，你会发现，Waterfall 这一栏下，蓝色的线代表的是DOM 加载完毕的节点，而红色的线代表的是 load 脚本执行结束的节点。
:::

### 1. Filter

刚刚提到，面板上已经内置了一个 filter 帮助过滤请求:

过滤器的输入框接受字符串，或正则表达式，会显示匹配条件请求。 

你还可以输入 例如 `method` 或者 `mime-type` 这样的条件来试试:

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/network-search.gif)

如果想筛选，但是又不知道支持哪些筛选条件，可以输入 `-` 来查看所有的条件：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/network-search02.png)

### 2. Preserve log

`Preserve` （保留）日志，在什么时候会用到呢？当需要记录页面刷新前后的 log 或者是页面跳转前后的 log 来进行对比调试的时候。

它会一直保留之前的日志，无论是刷新还是页面的跳转：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/Preserve_log.gif)

### 3. 多类型筛选

当你筛选出一大堆的 log 记录，但只想看关于 `JavaScript` 和 `CSS` 的请求的时候怎么做呢？

按住 `cmd` ，然后鼠标左键选择你想添加筛选的类目：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/select.gif)

### 4. 查看未压缩的文件体积

在 `Network` 面板中可以很直观的看到文件的体积，但是如果我想看到未压缩的体积呢？

只需要在 `Network` 面板中设置 `Use large request rows` :

![](https://wingman-1300536089.file.myqcloud.com//chrome/C04/large_request_rows.gif)

刷新页面发现，这张图的大小是 `29.7kb` 但是实际上网络传输的体积只有 `29.3kb` 。

原因就在 `Response header` 里面：这张图在 `Nginx` 中配置了 `gzip` 压缩。
