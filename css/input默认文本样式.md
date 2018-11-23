---
title: input默认文本样式
tags: 
    - html
    - css
categories: css
---

## 使用一般方法,如下:
<!-- more -->
```style
    input::-webkit-input-placeholder{}    /* 使用webkit内核的浏览器 */
    input:-moz-placeholder{}                  /* Firefox版本4-18 */
    input::-moz-placeholder{}                  /* Firefox版本19+ */
    input:-ms-input-placeholder{}           /* IE浏览器 */
```