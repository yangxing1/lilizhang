---
title: angular4 将html字符串渲染到dom元素
tags: 
    - javascript
    - ionic
    - ionic3
    - 指令
    - html
categories: javascript ionic html innerHTML
---

第一步用指令绑定的方法. 将字符串绑定到innerHTML这个属性上.得到正确的解析(浏览器解析), 第二步使用内置解析api将被转义后的字符串转为html文本
<!--more-->

```html
    <!-- angular的指令绑定属性写法 -->
    <div [innerHTML]="toHtml(user_cont)"></div>
```

```javascript
    // 一个页面类
    export class memberUser {
        // 注入解析api
        constructor(public sanitizer:DomSanitizer) {

        }
        toHtml(str) {
            str = '' + str; // 把str这个变量加入到String()这个类的原型链的末尾
            // 将<这个字符还原
            var temp_str =  str.replace(/&lt;/g, "<").replace(/&gt;/g, ">").replace(/&amp;/g, "&").replace(/&quot;/g, '"').replace(/&apos;/g, "'");
            // 解析字符串为html文本
            return this.sanitizer.bypassSecurityTrustHtml(str);
        }
    }
```