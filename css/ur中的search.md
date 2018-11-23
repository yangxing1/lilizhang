---
title: url中的search
tags: 
    - javascript
categories: javascript
---

## 使用window.location.search可以得到url中的条件查询，一个url可以使用多个条件，如下：
<!-- more -->

```javascript
console.log(window.location.search);
// ?id=0&type=read
// 使用&隔开每个条件
```
