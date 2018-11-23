---
title: table td宽度设置
tags: 
    - html
    - css
categories: css
---

## 默认根据内容设置td(列)宽度, 但是可以使用max-width固定:
<!-- more -->
```sheetstyle
    table {
        
    }
    table td {
        max-width:100px;
        min-width:100px;
    }
```

## 还可以根据第一行设置宽度, 后面行跟随:
```sheetstyle
    table {

    }
    table th {
        width:100px;
    }
```