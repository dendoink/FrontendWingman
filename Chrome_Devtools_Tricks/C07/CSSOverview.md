::: quote
在 element 面板你可以检查每个元素的 CSS，那有没有办法看到整个页面的 CSS 概览呢？
:::

::: warning 请注意
这是一个实验中的功能，有可能会导致一些问题。
:::

想看到有关页面的所有的 CSS 信息，你需要用到这个实验中的功能：

* 打开设置，勾选 CSS 概览：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C07/css_over_view01.gif)

* 重新打开 `devtools` 就可以看到啦：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C07/css_overview_02.gif)

这个面板主要包含这些信息：

### 1. CSS 的概览

汇总：

* 元素数量数量
* 行内样式的元素数量
* 样式规则数量
* 媒体查询的数量
* 类型选择器数量
* ID 选择器数量
* 类选择器数量
* 属性选择器数量
* 通配选择器数量

...

### 2. 颜色

汇总了：

* 背景颜色
* 文本颜色
* 填充颜色
* 边框颜色

最关键的是，这里出现的每一种颜色，你点进去都是它对应的 `CSS` 定义！

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C07/css_overview_color.gif)

这极大的方便了你找到那些和设计稿不兼容的颜色，大部分时候你都是靠全局搜索和肉眼去搜索。

### 3. 字体信息

不同字体类型的统计信息，分为字体大小，字重和行高三个维度。和颜色一样，都可以跳转到具体样式定义：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C07/css_over_view_font.gif)

### 4. 未使用的定义

同样可以点进去看看为什么没有被用到，对于优化代码有很大的帮助：

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C07/css_over_view_unused_declaration.png)

### 5. 媒体查询

一般我们都会做多端适配，有一种普遍的方式是使用媒体查询，但是你知道有哪些会影响到当前页面吗？

![](https://wingman-1300536089.cos.ap-shanghai.myqcloud.com/chrome/C07/css_over_view_media_query.gif)
