---
title: ionic3 使用navtion插件的时候没办法注入
tags: 
    - javascript
    - ionic
    - ionic3
    - 指令
    - html
categories: javascript ionic html innerHTML
---

ionic3 使用插件但是安装的却是ionic4的代码, 所以会造成官方文档写错的情况发生
<!--more-->

```javascript
    // 原来的写法
    import { QRScanner, QRScannerStatus } from '@ionic-native/qr-scanner';
```

```javascript
    // 新的写法
    import { Camera } from '@ionic-native/camera/ngx';
```