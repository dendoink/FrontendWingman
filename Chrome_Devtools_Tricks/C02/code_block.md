::: quote
如果我想看看，当前页面内所有 `p` 标签包含的文字总数，应该怎么做呢？
:::

### 例子

在 Chrome 中使用 `JavaScript` 作为自动化工具，可以效率地处理网站数据，比如开头的问题，你可以这样解决：

``` javascript
$$('.theme-default-content p')
    .map(el => parseInt(el.innerText.length))
    .reduce((sum, value) => sum + value)
```

在 `Console` 面板运行这段代码，会得到这样的返回值:

![](https://wingman-1300536089.file.myqcloud.com//chrome/C02/code-block.png)

这样的脚本，并不需要花费我太多的精力来写，但只是偶尔用用。所以我并不愿意每次都自己写。

那怎么解决这个问题呢？

这就是 `Snippets` 的用武之地了：通过它可以存放 `JavaScript` 代码到 `DevTools` 中，方便下一次使用：

* 进入到 `Sources` 面板
* 在导航栏里选中 `Snippets` 这栏
* 点击 `New snippet(新建一个代码块)` 
* 输入你的代码之后保存

大功告成！现在通过右击菜单或者快捷键： `[ctrl] + [enter]` 来运行你刚刚保存的脚本吧：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C02/code-snippet.gif)

### 1. 运行其他来源的代码块

当我在 `DevTools` 中预设了一组很棒的代码块以后，甚至都不需要打开 `Sources` 来运行它。

* 先给它取个好记的名字：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C02/snippet01.gif)

* 使用 `Command Menu` 快捷键 （ `[command] + [p]` ） ：在它的输入框中输入 `!` ，就可以根据名字来筛选预设代码块：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C02/snippet02.gif)
