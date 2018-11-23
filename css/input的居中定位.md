---
title: input的居中定位
tags: 
    - html
    - css
categories: css
---

## 如果一个容器内, 只有一个input标签, 那么对他的行高设置无效, 如下:
<!-- more -->
```html
    <style>
        div {
            height:36px;
            line-height:36px;
        }
        div input {
            display:inline-block;
            vertical-align:center;
        }
    </style>
    <div>
        <input type="radio" />
    </div>
```

## 可在容器上添加伪元素设置不可见修复, 如下:
```html
    <style>
        div:after {
            content:'占位符';
            display:inline-block;
            width:0;
            height:0;
            overflow:hidden;
        }
    </style>
```