---
title: ionic3手动获取input焦点
tags: 
    - javascript
    - ionic
    - ionic3
    - focus
    - 焦点
    - ElementRef
categories: javascript ionic
---

在ionic3的组件js里面获取一个input的焦点
<!--more-->

```javascript
export class MemberLoginPage {
    @ViewChild('passwordinput') password_input: ElementRef; // 得到input的dom对象(ionic封装)

    changePasswordShow(event) {
        this.password_input['setFocus']();  // 设置焦点事件
    }
}
```