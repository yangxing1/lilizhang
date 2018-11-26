---
title: js克隆对象的方法
tags: 
    - javascript
    - 对象
    - 赋值
    - 克隆
    - 序列化
categories: javascript JSON
---

对象赋值是用的指针赋值(引用赋值), 所以一个对象转手两三次后, 就无法分辨哪里修改了, 所以我们需要将一个对象完全复制成一个新的对象.
<!-- more -->

## 机灵的方法是用序列化转换一次就得到一个值相同但地址不同的对象, 但是缺点是序列化不能拷贝链式对象, 或者循环对象, 如下:
```javascript
var o = {};
o.a = [1];
o.b = 'hello';

var p = JSON.parse(JSON.stringify(o));
p.b = 'world';
p.a[0] = 2;

console.log(o.a);   // [1];
console.log(o.b);   // 'hello'
```

## 或者有更高的需求, 可以手动写一个clone()方法到Object.pretotype上.共用