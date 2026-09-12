---
layout: post
title: "Bugku CTF GET 传参"
date: 2026-09-12
categories: CTF
tags: [Bugku, Web, PHP, GET]
---
# 题目：GET
## 题目描述
访问页面，页面输出PHP源码：
```php
$what=$_GET['what'];
echo $what;
if($what=='flag')
echo 'flag{****}';

## 解题思路
$_GET['what'] 的作用是获取URL地址栏中what参数的值。当传入参数what=flag，满足代码中的if判断条件，页面就会输出flag。

## 解题过程
1. 打开靶机链接，页面展示PHP源代码。
2. 在原URL后面拼接GET参数：?what=flag
完整访问地址：
http://160.202.254.160:19879/?what=flag
3. 访问拼接后的链接，页面直接返回flag。

## Flag
flag{cle4072d1bdedeacle25b20afd9d49e0}

## 知识点总结
1. $_GET用来接收URL问号后携带的参数，浏览器直接访问网页默认就是GET请求。
2. GET传参格式：网址?参数名=参数值。
