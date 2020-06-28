::: quote
`Network` 作为调试中比不可少的一环，但你对它的了解有多少呢？
:::

打开 `Network` 你会看到很多的请求:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C04/network-overview.png)

但就是这样，你觉得上面的截图，好像没有缺少任何有效信息，但只是你看到了想看到的，有很多的关键信息在不起眼的位置：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C04/DOM_LOAD_Time.png)

为什么大部分时候没有注意到呢？因为 DOM 结构渲染的时间，和执行 load 脚本的耗时，是在已经完成功能的情况下进行性能优化的时候才会用到。

而我们工作的核心，就是通过过滤这个面板，找到那些我们需要的请求，然后查看它的详细信息，判断它是否正确得返回了我们需要的值。

:::tip 敲黑板
如果你细心的话，会发现，Waterfall 这一栏下，蓝色的线代表的是DOM 加载完毕的节点，而红色的线代表的是 load 脚本执行结束的节点。
:::

### 1. Filter

面板上内置了一个 filter 让我们来过滤请求:

filter 的输入框接受字符串或正则表达式，对应显示匹配的请求。 但也可以用它来过滤很多属性。

你可以输入 例如 `method` 或者 `mime-type` 来试试:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C04/network-search.gif)

如果你想筛选，但是又不知道支持哪些筛选条件，可以输入 `-` 来查看所有的条件：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C04/network-search02.png)

### 2. Preserve log

`Preserve` （保留）日志，在什么时候会用到呢？当你需要记录页面刷新前后的 log 或者是页面跳转前后的 log 来进行对比调试的时候。

它会一直保留你之前的日志，无论是刷新还是页面的跳转：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C04/Preserve_log.gif)

### 3. 多类型筛选

当你能够筛选出一大堆的 log 记录，但是你只想看关于 JavaScript 和 CSS 的请求 log 怎么做呢？

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C04/select.gif)

### 4. 查看未压缩的文件体积

我们在 `Network` 面板中可以很直观的看到文件的体积，但是如果我想看到未压缩的体积呢？

我们需要在 `Network` 面板中设置 `Use large request rows` :

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C04/large_request_rows.gif)

刷新页面之后发现，这张图的大小是 `29.7kb` 但是实际上网络传输的体积只有 `29.3kb` 然后再进入到 `Response header` 里面看到因为这张图在 `Nginx` 中配置了 `gzip` 压缩。
