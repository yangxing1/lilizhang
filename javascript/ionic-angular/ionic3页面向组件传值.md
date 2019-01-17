---
title: ionic3页面向组件传递值
tags: 
    - javascript
    - ionic
    - ionic3
    - component
    - 组件
categories: javascript ionic
---

页面向组件传递值, 组件的构造函数是获取不到传递过来的值, 只能在组件加载完成, 后才能获得这个值
<!-- more -->
```javascript
    @Input() mcType:string = 'highprice';  // 商品的类型
    constructor() {
        console.log(this.mcType);       // undefined
    }
    ngOnInit() {
        console.log(this.mcType);       // 传递过来的值
    }
```