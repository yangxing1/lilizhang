---
title: ionic3懒加载使用
tags: 
    - javascript
    - ionic
    - ionic3
    - IonicPage
    - 懒加载
    - 指令
    - 服务
categories: javascript ionic
---

使用懒加载后, 将每个页面视为单独的appmodule, 如果需要使用公共的指令, 组件, 服务, 管道都需要在页面的module里面先导入, 否则找不到
<!--more-->

```javascript
    import { NgModule } from '@angular/core';
    import { IonicPageModule } from 'ionic-angular';
    import { ProductDetailsPage } from './product-details';
    import { ComponentsModule } from '../../components/components.module';
    import { PipesModule } from '../../pipes/pipes.module';
    import { DirectivesModule } from '../../directives/directives.module';

    @NgModule({
        declarations: [
            ProductDetailsPage,
        ],
        imports: [
            IonicPageModule.forChild(ProductDetailsPage),
            ComponentsModule,
            PipesModule,
            DirectivesModule
        ],
    })
    export class ProductDetailsPageModule { }
```