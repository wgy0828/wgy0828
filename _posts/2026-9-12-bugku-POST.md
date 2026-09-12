---
layout: post
title: "Bugku CTF POST 传参"
date: 2026-09-12
categories: CTF
tags: [Bugku, Web, PHP, POST]
---
## 题目：POST
## 题目描述
访问页面，页面输出PHP源码：
```php
$what=$_POST['what'];
echo $what;
if($what=='flag')
echo 'flag{****}';

## 解题思路
$_POST['what'] 用于接收POST请求体中的参数。构造POST请求传入what=flag，满足代码的判断条件，页面输出flag。

## 解题过程
1. 访问靶机页面，页面展示PHP源代码。
2. 使用curl工具发送POST请求，参数设置为what=flag：
curl -X POST -d "what=flag" http://160.202.254.160:11729
3. 执行命令，读取返回页面内容，获取flag。

## Flag

flag{a895d0bfe0c73f3efd32e637bce539db}

## 知识点总结
1. $_POST 获取请求体内提交的表单参数。
2. curl命令可以直接构造POST请求，向服务端提交数据。
3. 浏览器直接访问网页默认发送GET请求，无法触发POST参数接收逻辑。
