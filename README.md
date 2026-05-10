# 苏超多路直播墙

一页看全多场苏超直播。打开网页，填入场次 ID，系统会自动排成最适合观看的电视墙：单场专注、双场并看、三场横排、四场 2x2、六场 3x2。

[立即打开](https://jamesju1987.github.io/suchao/)

![苏超多路直播墙营销海报](assets/marketing-poster.png)

单独二维码：

![苏超多路直播墙二维码](assets/qr-suchao.png)

## 为什么好用

- **打开即用**：纯静态网页，无需安装、无需登录后台。
- **场次灵活**：支持 `1 / 2 / 3 / 4 / 6` 场比赛展示，输入多少场就自动适配。
- **操作直观**：顶部输入场次 ID，点“应用”即可换一组比赛。
- **画面友好**：默认完整显示直播画面，必要时可切换“区域填满”，只在当前区域内放大。
- **适合大屏**：自动网格、主画面、纵向布局都内置好了，现场值守和办公室看盘都方便。

## 快速使用

直接访问：

```text
https://jamesju1987.github.io/suchao/
```

也可以把场次写进 URL：

```text
https://jamesju1987.github.io/suchao/?turnId=200&ids=41
https://jamesju1987.github.io/suchao/?turnId=200&ids=41,42
https://jamesju1987.github.io/suchao/?turnId=200&ids=41,42,43
https://jamesju1987.github.io/suchao/?turnId=200&ids=41,42,43,44
https://jamesju1987.github.io/suchao/?turnId=200&ids=41,42,43,44,45,46
```

## 布局规则

| 场次数 | 自动布局 |
| --- | --- |
| 1 场 | 单画面 |
| 2 场 | 左右双画面 |
| 3 场 | 一行三画面 |
| 4 场 | 2x2 |
| 6 场 | 3x2 |

如果误填 5 个场次，页面会自动补到 6 个，避免出现不均衡的电视墙布局。

## 参数说明

- `turnId`：轮次 ID，默认 `200`
- `ids`：比赛场次 ID，用英文逗号分隔
- `layout`：布局模式，可选 `equal`、`focus`、`stack`
- `focus`：主画面索引，从 `0` 开始

示例：

```text
https://jamesju1987.github.io/suchao/?turnId=200&ids=41,42,43,44,45,46&layout=equal
```

## 部署

项目已经适配 GitHub Pages，仓库根目录直接发布即可。
