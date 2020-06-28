::: quote
设置的断点是不是被执行了太多次？
有一个包含 `150` 个元素的循环，但我只想知道第 `120` 次循环的结果？
:::

### 1. `Conditional breakpoints` 条件断点

``` javascript
let result = 0;
Array.from(Array(150)).map(Math.random).forEach((vaule, index) => {
    result += v * index
})
```

想知道第 `120` 次的执行结果，除了循环到 `120` 次，还有别的办法吗？

* 右击行号，选择 `Add conditional breakpoint...(添加条件断点)` 
* 或者右击一个已经设置的断点并且选择 `Edit breakpoint(编辑断点)` 
* 然后输入一个执行结果为 `true` 或者 `false` 的表达式（它的值其实不需要完全为 `true` 或者 `false` 尽管那个弹出框的描述是这样说的）。

在这个表达式中，你可以使用任何这段代码可以获取到的值（当前行的作用域）。

条件成立就会暂停代码的执行：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/conditional_breakpoints.gif)

### 2. The ninja（忍者） `console.log` 

得益于条件断点， `console.log` 也有了新玩法：

* 每一个条件都必须经过判断 - 当应用执行到这一行的时候进行判断
* 并且如果条件返回的是 `falsy` 的值(这里的 `falsy` 并非是笔误， `falsy` 指的是被判定为 `false` 的值，例如 `undefined` )，它并不会暂停..

与其在你的源码的不同地方去添加 `console.log` / `console.table` / `console.time` 等等，不如你直接使用条件判断来将它们“连接”到 `Source` 面板中。
这样它们就会一直执行，而不当不再需要它们的时候，在 `Breakpoints section` 点两下鼠标，就可以把所有的断点都移除，就像一堆忍者一样突然消失！

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/ninjalog.gif)

> 这个技术在调试生产环境的问题时同样很有用，因为你通过这样的方式轻松将 `console logs` 插入到 `source` 里。
