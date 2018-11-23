---
title: ionic小知识,偏门知识,不容易遇到的问题
tags: 
    - javascript
    - ionic
    - 偏门
    - 小知识
categories: javascript ionic
---

各种不容易遇到的ionic上的使用问题, 和偏门小知识, 这里做一个集合
<!-- more -->

## 一, 渲染一个注入的模块里面的属性或者变量时无效, 如下
```javascript
    // 注意这里是ionic1.1版本
    .controller('UserProfileCard', ['$rootScope', '$scope', 'ENV', function($rootScope, $scope, ENV) {
        console.log(ENV.a);         // 'hello world'
    }])
```
```html
    <p>{{ENV.a}}{{ENV.b}}</p>
```

结果是无法渲染到html上, 解决办法是将模块里的属性重新声明到当前作用域里
```javascript
    .controller(''[function(ENV) {
        $scope.a = ENV.a;               // 重定向到这里就可以渲染到html
    }])
```