---
title: angular4 的管道使用
tags: 
    - javascript
    - ionic
    - ionic3
    - pipes
    - 管道
categories: javascript ionic
---

管道的创建和使用参照官方文档
<!--more-->
```javascript
import { WebSitePipe } from '../pipes/web-site/web-site';
@NgModule({
    declarations: [ WebSitePipe ]
});
```

### 坑爹的地方是, 新建管道后, 在app.module里面导入了(管道,或管道模块)之后. 在预编译的页面上可以直接使用. 如果是懒加载页面必须在页面的module里面导入这个管道
```html
<h2>{{title|imgUrl}}</h2>
```


### 懒加载页面使用管道

懒加载和预编译页面不同, 预编译模板在app.module里面导入管道模块就能使用, 懒加载必须在页面module里面导入
```javascript
/* product-details.module.ts */
import { PipesModule } from '../../pipes/pipes.module';
@NgModule({
    imports:[PipesModule]
})
```

```html
<!-- product-details.html -->
<h2>{{title|imgUrl}}</h2>
```

### 组件内使用管道

组件里面使用管道和页面不同, 组件需要在components.module.ts里面导入管道模块才能使用, 页面导入的模块并不会给到组件上

```javascript
/* components.module.ts */
import (PipesModule) from '../pipes/pipes.module';
@NgModule({
    imports: [PipesModule],
});
```