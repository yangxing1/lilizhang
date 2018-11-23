---
title: 设置和获取html属性
tags: 
    - javascript
categories: javascript
---

## 使用原生js获取元素对象的属性使用getAttribute()方法，设置属性使用setAttribute()方法，如下：
<!-- more -->

```javascript
var $box = document.getElementById('box');
var str = $box.getAttribute('title');
$box.setAttribute('title', '2016-01-01');
```
