---
layout:     post
title:      "On The Ocean"
subtitle:   " \"Hello World, Hello Ocean\""
date:       2019-06-10 21:04:00
author:     "Abu"
header-img: "img/post-bg-2015.jpg"
catalog: true
tags:
    - Life
---

> "一百万个可能，庆幸MacBook和iPhone上都Download了Eudic，比Apple原生的英语词典好用多了，关键在于不需要任何配置就可以离线查询。"

## 前言

[跳过废话，直接看重点](#build) 

海上的生活简直就是原始的人间天堂，享受这里的生活，刚收到工资信息的我（刚才有点网络，然后过了半小时又没了），在船上拿着工资潇洒度日，可以读书、写作、海景房（尽管有点小）、吹吹海风（尽管后甲板的垃圾味道有点重），但这都不重要，在这里能够思考技术的底层，能够回望人生的点滴，能够展望未来的美好，下船后将是一次本质的升华。

<p id = "build"></p>
---

## 正文
### 关于技术

0）freeIPA的使用：
基于LDAP+KBOS的身份认证系统，uid不允许存在特殊字符，必须是纯英文字母。
administrator admin root DevOps00

|服务平台|认证|备注|
|:--:|:--:|:--:|
|ubuntu 16.04|KBOS|操作系统统一认证|
|centos 7.6|KBOS|操作系统统一认证|
|Jenkins|LDAP|基于java开发的CI模块，已经开启LDAP，m.liu用户为超级管理员|
|Rancher|LDAP|基于Go开发的CD模块，未开启LDAP，mliu用户为超级管理员|
|ZenTao|LDAP|基于PHP开发的ERP|
|ODOO|LDAP|CRM|
|Azure Portal|AD&LDAP|IaaS&PaaS服务商|
|Nginx|LDAP|采用nginx-ldap模块完成|
|Go|LDAP|运维平台使用go语言开发，前端集成ldap|

1）Filebeat+kafka+ELK+nginx+ldap，这套日志系统的部署应该及时完成

2）AKS部署一套代码



