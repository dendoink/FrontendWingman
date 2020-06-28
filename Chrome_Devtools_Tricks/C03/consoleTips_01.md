::: quote
我最开始接触前端的时候，学会用的就是 `console.log` ，甚至现在，大部分情况也还在用它调试，但不同的场景下，其实有更多好用的 API。
:::

### 1. `console.assert` 

设想你遇到这样的情况：当某个值判断为假(空字符串，undefined 或者 null)的时候，你期望能在 log 中把它打印出来：

一般的写法是这样：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/if-log.gif)

没有任何问题，就是不够优雅，优雅的写法应该是怎样呢：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/console_assert.gif)

:::tip 敲黑板
当我们传入的第一个参数为 **假** 时， `console.assert` 打印跟在这个参数后面的值。
:::

:::warning 请注意
请注意，**如果你使用的 `NodeJS` 版本 `≤ 10.0` ， `console.assert` 可能会中断后面代码的执行**，但是在 `.10` 的版本中被修复了(当然，在浏览器中不存在这个问题)
:::

### 2. 增强 `log` 的阅读体验

假如有这么一堆看起来并不易读的数据要打印在 console 里面：

``` javascript
const name = "frontend-wingman"
const url = "www.frontendwingman.com"
const chapter = "console"
```

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/logObject.png)

光看输出的结果，我们很难判断打印的到底是哪个变量，为了让它变得更加易读，你可以打印一个对象：

* 将所有 `console.log` 的参数包装在大括号中。

``` javascript
console.log({name, url, chapter})
```

:::tip 敲黑板
原理就是 `ES6` 中[增强的对象字面量](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Object_literals) ，所以只要加上 `{}` 就完事儿了：
:::

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/logObject01.png)

### 3. `console.table` 

`console.table` 这个小技巧在开发者中可能并没有多少人知道: 

`console.table` 可以将 **数组** (或者是 **类数组** 的对象，或者就是一个 **对象** )打印成一个漂亮的表格。

它不仅会根据数组中包含的对象的所有属性，去计算出表中的列名，而且这些列都是可以 **缩放** 甚至 **还可以排序!!!**

如果你觉得展示的列太多了，使用第二个参数，传入你想要展示的列的名字:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/console_table.gif)

:::tip 敲黑板
对于后台而言，只有 `node` 版本大于 `10` 以上， `console.table` 才能起作用
:::