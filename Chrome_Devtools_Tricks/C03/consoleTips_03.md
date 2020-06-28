::: quote
如果我们想看到打印的时间戳呢？
:::

### 1. 给 `logs` 加上时间戳

这就用到了计时的相关操作：

要给应用中发生的事件, 加上一个确切的时间戳，需要开启 `timestamps` 。

你可以在设置(在调试工具中的 `⋮` 下拉中找到它，或者按下 `F1` )中来开启。

但是我建议你使用 `Commands Menu` 

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/console_timestamp.gif)

### 2. 监测执行时间

与其在所有事上展示一个时间戳，或许你对脚本中的特殊的节点之间执行的时间跨度更加感兴趣，对于这样的情况，我们可以采用一对有效的 `console` 方法

* `console.time()` — 开启一个计时器
* `console.timeEnd()` — 结束计时并且将结果在 `console` 中打印出来

如果你想一次记录多件事，可以往这些函数中传入不同的标签值。(例如: `console.time('loading')` ， `console.timeEnd('loading')` )

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/console_time_end.gif)


### 3. 让 `console.log` 基于调用堆栈自动缩进

配合 `Error` 对象的 `stack` 属性，让你的 `log` 可以根据堆栈的调用自动缩进：

``` javascript
function log(message) {
    console.log(
        // 这句话是重点当我们 new 出来的 Error 对象时，会匹配它的stack 信息中的换行符，换行符出现的次数也等同于它在堆栈调用时的深度。
        ' '.repeat(new Error().stack.match(/\n/g).length - 2) + message
    );
}

function foo() {
    log('foo');
    return bar() + bar();
}

function bar() {
    log('bar');
    return baz() + baz();
}

function baz() {
    log('baz');
    return 17;
}

foo();
```

运行结果如下：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/console_stack.png)