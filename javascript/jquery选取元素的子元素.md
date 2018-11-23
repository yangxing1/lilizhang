---
title: 选取子元素
tags: 
    - javascript
categories: javascript
---

## jquery使用$()选取元素，可以给$()传递第二个参数作为查找的上下文，如下：
<!-- more -->

```javascript
var $box = $('.box');
var $boxChild = $('.boxChild', $box);
```
