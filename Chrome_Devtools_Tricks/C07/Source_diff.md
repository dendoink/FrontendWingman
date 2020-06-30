::: quote
看完 worksapce 的介绍，我们可以把改动同步到本地的文件中，但是对于修改了什么，以及哪些是新增的部分，还是会模糊不清对吗？
:::

### 1. Source diff

::: warning 请注意
这是一个实验中的功能，有可能会导致一些问题。
:::

虽然这是一个实验中的功能，但是经过测试，我觉得他真的很好用，如果你喜欢使用 `workspace` 来编写代码，那这个功能一定对你有所帮助，首先我们需要在设置中打开这个功能：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C07/sourcediff_01.gif)

:::warning 请注意
当你打开这个选项之后，请务必在 **新的标签页重新打开** `devtools` 以确保此选项能够生效！
:::

### 2. Source diff 使用

首先你需要有一个本地的项目，你可以把它拖到 `Source` 或者按 `+` 号来选择对应的文件目录：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C07/sourcediff_02.gif)

:::tip 提示
如果你还不知道如何使用 `workspace` 可以看[这里](https://www.frontendwingman.com/Chrome/C06/workspaceTips.html)~
:::

当我们启用了 Source diff 之后：

* 紫色代表：修改的内容
* 红色代表：删除的内容
* 绿色代表：新增的内容

### 3. 配合 Drawer 的 changes 使用

Source diff 配合 Drawer 的 changes 使用效果更佳：

![](https://wingman-1300536089.file.myqcloud.com//chrome/C07/sourcediff_03.gif)

:::tip 敲黑板
当然你也可以使用命令打开 Drawer chanegs，如果你忘记了怎么打开可以看[这里]()
:::
