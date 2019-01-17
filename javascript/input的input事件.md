---
title: input的input事件
tags: 
    - javascript
    - input
    - 事件
    - 输入
categories: javascript
---

input标签的输入事件, 有时候就是用不起来
<!-- more -->

## 使用jquery调用的时候
```javascript
// propertychange 属性修改事件, 也可以触发
$('.input').on('input', function(e) {
    console.log('input');
});
```

## 使用原生调用
```javascript
var input_dom = document.getElementById('asdf');
input_dom.oninput = input_dom.onpropertychange = function(e) {
    console.log('input');
}
```