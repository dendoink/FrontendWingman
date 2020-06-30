::: quote
我们刚刚看到了 `console.table` 这个技巧，也了解了在他上面的 `{}` ，那么我们为什么不将他们结合起来打造一个终极 `log` 呢？
:::

### 1. table 和 `{}` 的配合

```javascript
console.table({name, url, chapter})
```

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/console_table_obj.png)

### 2. `console.dir` 

有时候你想要打印一个 `DOM` 节点。 `console.log` 会将这个交互式的元素渲染成像是从 `Elements` 中剪切出来的一样。如果说你想要查看 **这个节点所关联到的真实的js对象** 呢？并且想要查看他的 **属性** 等等？

在那样的情况下，就可以使用 `console.dir` :

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/console_dir.png)

### 3. 给你的 `console.log` 加上 `CSS` 样式

如果你给打印文本加上 `%c` 那么 `console.log` 的第二个参数就变成了 `CSS` 规则，试试看：

``` javascript
console.log('%c FE-Wingman! ', 'background: #222; color: #FFFFFF;font-size:3rem');
```

![](https://wingman-1300536089.file.myqcloud.com//chrome/C03/logincolor.png)