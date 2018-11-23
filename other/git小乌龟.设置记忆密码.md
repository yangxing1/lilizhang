---
title: git小乌龟记忆密码
tags: 
    -   git
    -   github
    -   小乌龟
    -   记忆密码
categories: git
---

在使用git(小乌龟, 不使用小乌龟的狠人输密码是很平常的)的时候老是输密码很烦, 故找到一个设置记忆密码输入一次密码就ok
<!-- more -->

## 设置选项 右键git设置>Git>Edit local .git/config>编辑器

```
[rebase]
	autosquash = true
[credential]
    helper = store 
```

添加此代码保存