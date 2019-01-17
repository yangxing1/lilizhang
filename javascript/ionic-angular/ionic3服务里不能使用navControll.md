---
title: ionic3(angular4)的provider(服务)NavController(路由器)
tags: 
    - javascript
    - ionic
    - ionic3
    - 版本
    - provider
    - NavController
categories: javascript ionic
---

在一个服务里面注入路由器模块(报错), 无法找到这个路由器模块(NavController), 可以注入App模块, 获取当前活动页面路由(appCtrl.getActiveNav()), 然后跳转
<!--more-->
```javascript
// bad
import { Injectable } from '@angular/core';
import { NavController, AlertController } from 'ionic-angular';
@Injectable()
export class LoginStatusProvider {
    // public login_info:any;
    private activeNav:NavController;
    constructor(public storage: StorageProvider, public appCtrl: App, public navCtrl: NavController) {
        // console.log('Hello MemberInfoProvider Provider');
        // this.activeNav = this.appCtrl.getActiveNav();
    }
    jump() {
        this.navCtrl.push('helloPage');// 报错无法找到NavController
    }
}
```


```javascript
// good
import { Injectable } from '@angular/core';
import { NavController, App } from 'ionic-angular';
@Injectable()
export class LoginStatusProvider {
    // public login_info:any;
    private activeNav:NavController;
    constructor(public storage: StorageProvider, public appCtrl: App) {
        // console.log('Hello MemberInfoProvider Provider');
        this.activeNav = this.appCtrl.getActiveNav();
    }
    jump() {
        this.activeNav.push('helloPage');
    }
}
```