---
title: css3 制作箭头实心
tags: 
    - html
    - css
    - 箭头
    - border
categories: css
---

## 使用纯css制作箭头
<!-- more -->
```style
.tip:before {
    content:'';
    width:0;
    height:0;
    border-style:solid;
    border-width:10px 10px;
    border-color:transparent transparent transparent #000;
    position:absolute;
    bottom:0;left:15px;
}
```

使用伪类做一个只有边框的正方形(长方形亦可), 然后一条边有颜色.其他所有边都为透明, 箭头即可