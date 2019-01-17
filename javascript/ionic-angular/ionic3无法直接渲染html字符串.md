---
title: ionic3不能直接渲染html字符串
tags: 
    - javascript
    - ionic
    - ionic3
    - html
    - string
categories: javascript ionic
---

没办法直接[innerHTML]=""这样渲染字符串, 可以使用内置的html解析器(DomSanitizer模块里的bypassSecurityTrustHtml方法)
<!--more-->
```javascript
    import { DomSanitizer } from '@angular/platform-browser';
    export class ProductDetailsPage {
        inner_html:string;
        constructor(private sanitizer: DomSanitizer) {
            this.inner_html = '<p>hello</p>';
            this.inner_html = this.sanitizer.bypassSecurityTrustHtml(this.inner_html);
        }
    }

```