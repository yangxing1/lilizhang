---
title: flex的使用
tags: 
    - html
    - css
    - 分列
    - flex
categories: css
---

## 在使用flex的时候, 对子项目的属性不是特别好记, 如下:
<!-- more -->
```html
    <div>
        <a>hello</a>
        <a>world</a>
    </div>
    <style>
        div {
            display:flex;
        }
        div > a {
            flex-grow:0;
            flex-shrink:0;
            flex-basis:auto;
            order:1;
        }
    </style>
```

### 各个属性的作用

flex-grow属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。如果其他项为1, 当前项为2就会占用两倍位置

flex-shrink属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。如果其他项为1, 当前项为0就不会缩小

flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小

order属性定义项目的排列顺序。数值越小，排列越靠前，默认为0。

### 参考

[ChokCoco的个人博客](https://www.runoob.com/w3cnote/flex-grammar.html)