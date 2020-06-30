::: quote
`Drawer` 中有一项叫 `Animations` 说真的我之前几乎没用过，但是了解之后才发现这功能太棒了!
:::

### 1. `Animations` 检查动画

当你看到一个很酷炫的动画，但它是好几个元素同时变化组成的，这种情况很难通过检索 element 的方式来弄懂它的原理是什么，这时候就可以使用 `Drawer` 慢速播放、重播或检查动画组的源代码：

上一小节已经说过如何打开 `Animation` 了，打开之后，只需要触发对应的动画：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C06/689_showanimation_01.gif)

你可以在 overview 面板里选择对应的动画组

:::tip 敲黑板
`动画组` : 动画检查器会根据开始时间（不包括延迟等等）检测哪些动画是相关的并将它们分到一组。换句话说，在同一脚本块中触发就被分为同一组，但如果是异步的，它们将单独分组。
:::

![](https://wingman-1300536089.file.myqcloud.com//chrome/C06/689_showanimation_02.gif)

可以选择播放速度的百分比[如果按下蓝色的循环按钮，动画就会循环播放]：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C06/689_showanimation_05.gif)

位于 Detail 面板左边的列表中会列出所有参与这个动画的 `DOM` 元素，并且在 element 面板和视窗中当前元素会被选中:

![](https://wingman-1300536089.file.myqcloud.com//chrome/C06/689_showanimation_03.gif)

:::tip 敲黑板
如果两个元素应用了同一个动画，它们会被分配相同的颜色。
:::

拖动第一个或最后一个圆圈, 修改动画持续时间:

![](https://wingman-1300536089.file.myqcloud.com//chrome/C06/animation_edit01.gif)

拖动白色内圈，更改关键帧的时间：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C06/animation_edit02.gif)
