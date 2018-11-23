---
title: css元素滚动但是删除滚动条
tags: 
    - html
    - css
    - scroll
    - 滚动条
    - overflow
categories: css
---

## 讲一个容器作为滚动元素. 但是将滚动条不显示, 使用如下样式:
<!-- more -->
```style
.div::-webkit-scrollbar {
	display: none;
}
```