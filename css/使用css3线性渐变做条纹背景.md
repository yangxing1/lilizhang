---
title: 使用css3线性渐变做条纹背景的用法
tags: 
    - css
    - css3
    - 条纹
    - 背景
categories: css
---

## 条纹背景最简单的方法就是使用背景图片,如下:

背景图片的条纹最好完整,高度和元素高度相同, 默认重复会铺满元素
<!-- more --> 

```style
.div {
    background:url("../stripe.jpg");
    background-size:100%; auto;
}
```

## 高级一点的用法是使用css3的样式,如下:

使用liner-gradient样式, 默认用法如下:

```style
.div {
    background:linear-gradient(#000,#ccc);
}
```

这个样式是渐变效果, 在元素上的表现为从黑色渐变为灰色, 将这个渐变取消, 给固定位置添加标记就可以做条纹效果, 如下:

```style
.div {
    background:linear-gradient(#000 50%,#ccc 50%);
}
```

添加一条设置背景大小的样式, 默认重复, 一个简单的条纹就ok, 如下:

```style
.div {
    background:linear-gradient(#000 50%,#ccc 50%);
    background-size:100% 25%;
}

切换方向, 如下:

```style
.div {
    background:linear-gradient(to right, #000 50%,#ccc 0);
    background-size:100% 25%;
}
```

可以将每一个重复的方块设置为条纹背景,这样就能实现倾斜的条纹, 如下:
```style
.div {
    background:linear-gradient(45deg, #000 25%,#ccc 0, #ccc 50%,#000 0, #000 75%, #ccc 0);
    background-size:40px 40px;
}
```

现在基本上的条纹都可以实现了, 但是现在不能调整倾斜的角度, 如果想要调整倾斜的角度可以使用repeating-linear-gradient, 如下:
```style
.div {
    /*如果需要更改角度*/
   background:repeating-linear-gradient(60deg,#000,#000 15px,#ccc 0,#ccc 30px);
   background-size:40px 40px;
}
```

---

### 参考

[张鑫旭的个人空间](https://www.zhangxinxu.com/wordpress/2011/04/%E5%B0%8Ftipcss3%E4%B8%8B%E6%9D%A1%E7%BA%B9%E6%96%B9%E6%A0%BC%E6%96%9C%E7%BA%B9%E8%83%8C%E6%99%AF%E7%9A%84%E5%AE%9E%E7%8E%B0/)

---

[Tiny_z的个人博客](https://www.jianshu.com/p/e8ee92bbb43f)