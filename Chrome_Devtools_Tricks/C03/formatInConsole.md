::: quote
有没有想过，在 `Chrome` 中用自己定义的格式来打印一个对象呢?
:::

### 1. Custom Formatter

自定义输出对象的函数，被称为 `Custom Formatter` 。

> 请注意: 在我们开始之前，需要在 `DevTools` 设置 (在 `DevTools` 的 `⋮` 下拉框找到设置，或者按下 `F1` ) 中把对应的选项打开:

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/Custom_Formatter.gif)

我们要定义的 `formatter` 是一个包含三个方法的对象：

* `header` : 处理如何展示在 `console` 的日志中的主要部分。
* `hasbody` : 如果你想显示一个用来展开对象的 `▶` 箭头，返回 `true` 
* `body` : 定义将会被显示在展开部分的内容中。

写完之后大概就是这样：
```javascript
window.devtoolsFormatters = [{
    header: function(obj){
        return ['div',{},`${JSON.stringfy(obj, null, 7)}`]
    },
    hasBody: function(){
        return false;
    }
}]
```

:::tip 敲黑板
例子里移除了循环结构的错误处理，让它看起来更加简洁
:::

`header` 方法返回了一个 [JsonML](http://www.jsonml.org/) (注： `JsonML` : `JSON Markup Language` - `JSON` 标记语言) 数组，由这些组成：

1. 标签名
2. 属性对象
3. 内容 (文本值或者其他元素)

(如果看起来很眼熟的话，那可能是因为你之前写过一些 [React 代码](https://reactjs.org/docs/react-without-jsx.html) : D)

在输出的时候，这个简单的 `formatter` 对于每一层嵌套，直接以 `7` 个空格的缩进打印这个对象。所以现在我们的输出看起来是这样：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/custom_formatter01.gif)

### 2. 应用实践

现有好几种 `custom formatter` 可供选择，例如：你可以在这个 [immutable-devtools ](https://github.com/andrewdavey/immutable-devtools) 仓库中找到对于 [Immutable.js](https://facebook.github.io/immutable-js/)  结构的完美展示。

工作中你遇到结构不寻常的对象时，或在大量的日志(最好避免这样的情况，但是有时候很有用)中去区分一些对象时，就可以采用 `custom formatter` 来处理。

小窍门：将你不关心的对象过滤出来，在 `header` 方法里面 `return null` 。让 `DevTools` 使用默认的格式化方式来处理这些值。

撇开实用性，我们还可以找点乐子：

`console.clown()` : 将打印对象进行转换，而且在对象前面加上一个 `emoji` 表情 ... 

源码：

``` javascript
window.devtoolsFormatters = [{
    header: function(obj) {
        if (!obj.__clown) {
            return null;
        }
        delete obj.__clown;
        const style = `
        color: red;
        border: dotted 2px gray;
        border-radius: 4px;
        padding: 5px;
      `
        const content = `🤡 ${JSON.stringify(obj, null, 2)}` ;

        try {
            return ['div', {
                style
            }, content]
        } catch (err) { // for circular structures
            return null; // use the default formatter
        }
    },
    hasBody: function() {
        return false;
    }
}]

console.clown = function(obj) {
    console.log({
        ...obj,
        __clown: true
    });
}

console.log({
    message: 'hello!'
}); // normal log
console.clown({
    message: 'hello!'
}); // a silly log
```

就像你看到的一样，使用 `console.clown` 方法打印出来的对象被添加了一个特殊的属性，方便我们将它区分出来。

平时自己用的话，建议你还是设置一个判断，检查这个对象是不是某一个特殊类的实例等等。

`clown` 打印出来了什么东西呢？

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C03/custom_result.png)
