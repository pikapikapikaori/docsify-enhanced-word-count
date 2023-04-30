<!--
 * @Author: pikapikapikaori pikapikapi_kaori@icloud.com
 * @Date: 2023-04-05 02:10:31
 * @LastEditors: pikapikapikaori pikapikapi_kaori@icloud.com
 * @LastEditTime: 2023-05-01 04:29:02
 * @FilePath: /docsify-enhanced-word-count/docs/README.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
# docsify-enhanced-word-count

<p align="center">
  <img src="https://docsify.js.org/_media/icon.svg" />
  <br />
  <code>docsify-enhanced-word-count</code>
</p>

![badge](https://img.shields.io/github/license/pikapikapikaori/docsify-enhanced-word-count) ![badge](https://img.shields.io/github/last-commit/pikapikapikaori/docsify-enhanced-word-count)

English | [中文](/zh-cn/)

This is a plugin to enhance [docsify-count](https://github.com/827652549/docsify-count) plugin.

## What Problem to Solve

Plugin docsify-count is a quite good plugin that provides for counting words in the article. However, it has a bad support for i18n localization as it can only set one language at the same time. As a result, if you have multiple languages in one docsify document, you can't set the displayed word/minute separately.

## After Using This Plugin

This plugin adds i18n localization support for docsify-count.

## To Use

In `index.html`, add:

```html
<!-- docsify-enhanced-word-count plugin -->
<script src="https://cdn.jsdelivr.net/gh/pikapikapikaori/docsify-enhanced-word-count/src/countWords.js"></script>
```

Add settings:

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

| Attribute    | Type    | Description                          | Value                     |
| ------------ | ------- | ------------------------------------ | ------------------------- |
| countable    | Boolean | Set whether to use this plugin       | true(Default) / false     |
| position     | String  | Set display position                 | 'top'(Default) / 'bottom' |
| margin       | String  | Set margin to the near DOM element   | '10px'                    |
| float        | String  | Set alignment                        | 'right'(Default) / 'top'  |
| fontsize     | String  | Set font size                        | '0.9em'                   |
| color        | String  | Set color                            | 'rgb(90,90,90)'           |
| localization | Object  | Support localization                 |                           |
| isExpected   | Boolean | Set whether to  display reading time | true(Default) / false     |

## Related Reference

1. [docsify-count](https://github.com/827652549/docsify-count)

## Others

It's welcomed to make pr to this repo in order to improve this plugin.

If you like this plugin, please give a star, thanks!

For more tools I developed please refer to [my blog](https://pikapikapikaori.github.io/pikapikapi-blog/#/en-us/ITtech/).
