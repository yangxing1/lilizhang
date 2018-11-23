---
title: nodeJs 创建事件
tags: 
    - 事件
    - EventEmitter
    - node
categories: node
---

## nodejs 自带一个事件机制

引用事件模块到当前页

<!-- more -->

```javascript
var EventEmitter = require('events').EventEmitter;
```

创建一个事件响应
```javascript
var event = new EventEmitter();
event.on('open_dir', function(file_arr) {
    console.log(file_arr);
})
```

触发事件
```javascript
setTimeout(function() {
    event.emit('open_dir', 'file_arr');
}, 2000)
```
