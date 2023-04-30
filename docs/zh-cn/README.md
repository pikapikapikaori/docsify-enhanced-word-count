# docsify-enhanced-word-count

<p align="center">
  <img src="https://docsify.js.org/_media/icon.svg" />
  <br />
  <code>docsify-enhanced-word-count</code>
</p>

![badge](https://img.shields.io/github/license/pikapikapikaori/docsify-enhanced-word-count) ![badge](https://img.shields.io/github/last-commit/pikapikapikaori/docsify-enhanced-word-count)

[English](/) | 中文

本插件用于增强[docsify-count](https://github.com/827652549/docsify-count)插件。

## 解决的问题

插件docsify-count是一款对统计文章字数非常有帮助的插件。但是，它对于多语言国际化的支持比较差。其全局只支持同时设置一种语言，因而，如果docsify文档中有多种语言的话，难以为其分别配置不同的语言。

## 本插件的使用效果

本插件在集成docsify-count的基础上为其提供了多语言国际化支持。

## To Use

`index.html`中添加:

```html
<!-- docsify-enhanced-word-count plugin -->
<script src="https://cdn.jsdelivr.net/gh/pikapikapikaori/docsify-enhanced-word-count/src/countWords.js"></script>
```

添加一下设置：

```js
window.$docsify = {
    ountWords: {
        countable: true,
        position: "top",
        margin: "10px",
        float: "right",
        fontsize: "0.9em",
        color: "rgb(90,90,90)",
        localization: {
            words: {
                '/zh-cn/': '字',
                '/': 'words'
            },
            minute: {
                '/zh-cn/': '分钟',
                '/': 'min'
            },
        },

        // Or
        // localization: {
        //     word: 'words',
        //     minute: 'min'
        // }

        isExpected: true,
    },
}
```

| 属性    | 类型    | 描述                          | 可选值                     |
| ------------ | ------- | ------------------------------------ | ------------------------- |
| countable    | Boolean | 是否使用本插件       | true(默认值) / false     |
| position     | String  | 展示位置                 | 'top'(默认值) / 'bottom' |
| margin       | String  | 设置距离上方元素的margin距离   | '10px'                    |
| float        | String  | 设置对齐                        | 'right'(默认值) / 'top'  |
| fontsize     | String  | 设置字体大小                        | '0.9em'                   |
| color        | String  | 设置字体大颜色                        | 'rgb(90,90,90)'           |
| localization | Object  | 支持国际化              |                           |
| isExpected   | Boolean | 设置是否展示预计阅读时间 | true(默认值) / false     |

## 相关资料

1. [docsify-count](https://github.com/827652549/docsify-count)

## Others

如果您有对本项目的优化，欢迎提交PR。

如果您喜欢本插件，可以给我点个star，谢谢！

我开发的一些其他工具可以参考[我的博客](https://pikapikapikaori.github.io/pikapikapi-blog/#/ITtech/)。
