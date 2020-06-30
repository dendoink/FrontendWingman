::: quote
在我们调试 `Javascript` 的代码时， `对象` 和 `方法` 作为经常被我们调试的对象，所以这里介绍关于 `对象` 和 `方法` 的调试技巧。
:::

### 1. `queryObjects` （对象查询）方法

``` javascript
class Person {
    constructor(name, role) {
        this.name = name;
        this.role = role;
    }
}

const jack_ma = new Person('Jack Ma', 'Dad')
const CEOS = [
    new Person('Pony Ma', 'CEO'),
    new Person('Richard LIU', 'CEO'),
]
```

假如我们有这样一段代码，我们在里面定义了一些对象。

在代码执行的 **某个特定的时刻** + **特定的执行上下文** 有哪些对象呢？

在 `DevTools` 里的 `queryObjects` 函数可以展示这些信息。

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/queryObjects.gif)

### 2. `monitor` 监控

每当一个被 `monitor` 的方法执行时， `console 控制台` 会打印当期被调用的 **函数名** 以及 **参数**：

例子

``` javascript
  function sum(x, y) {
      return x + y;
  }
  monitor(sum);
```

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/monitor.png)

我们可以少写很多 `console.logs` !

:::tip 敲黑板
执行 `unmonitor()` 可以停止对某一个函数的监控
:::

#### 3. `monitorEvents` 事件监控

在上文中，我们讨论了用 `monitor` 方法来监听函数，其实还可以使用名为 `monitorEvents` 的方法，对 `events` 做一样的事情：

当指定对象上发生指定事件之一时，事件对象将记录到控制台。

不光是单个事件，甚至是事件数组或事件集合的一般事件类型：

监视窗口对象上的所有调整大小事件：

```javascript
monitorEvents(window, "resize");
```

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/monitorEvents.gif)


你可以同时对 `resize` 还有 `scroll` 事件进行监听：

```javascript
monitorEvents(window, ["resize", "scroll"])
```


指定一种事件类型进行监听：



| 类型 | 事件                                                         |
| -------- | --------------------------------------------------- |
| mouse    | "mousedown", "mouseup", "click", "dblclick", "mousemove", "mouseover", "mouseout", "mousewheel" |
| key      | "keydown", "keyup", "keypress", "textInput"                  |
| touch    | "touchstart", "touchmove", "touchend", "touchcancel"         |
| control  | "resize", "scroll", "zoom", "focus", "blur", "select", "change", "submit", "reset" |


给当前选中的输入框，加上键盘事件的监听：

```javascript
monitorEvents($0, "key");
```

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/monitorEvents_key.gif)
