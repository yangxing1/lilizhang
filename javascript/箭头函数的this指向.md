---
title: 箭头函数的用法.及this指向
tags: 
    - javascript
    - 箭头函数
    - 函数
categories: javascript es6
---

在使用es6的新特性, 箭头函数时, 需要注意this的指向
<!-- more -->
```javascript
(function() {
    let a = 'hello';
    ()=>{
        console.log(this.a);    // 'hello';
    }
    let b = {
        a:'world'
    };
    b.func = ()=>{
        console.log(this.a);    // 'hello';
    }
    b.func();
    // 就算这个方法有上下文也不使用, 只指向当前作用域的this
})();

```