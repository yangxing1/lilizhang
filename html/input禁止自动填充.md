---
title: input禁止自动填充
tags: 
    - html
    - input
    - 密码
    - 自动填充
categories: html
---

## input自动填充禁止方法, 有隐藏input, 有焦点换类型, 最好用的是设置autocomplete="new-password", 如下:
<!-- more -->
```html
    <input type="password" autocomplete="new-password" />
```