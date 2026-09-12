---
layout: post
title: "Bugku CTF alert Writeup"
date: 2026-09-12
categories: CTF
tags: [Bugku, WEB, alert弹窗, ASCII编码]
---
# 题目：alert
## 题目描述
访问网页会无限弹出alert弹窗，干扰浏览页面，提示flag就在这里。
## 解题思路
考点：JS弹窗干扰 + HTML注释存放ASCII编码。
页面用大量alert弹窗干扰用户，flag藏在网页源码底部HTML注释内，是一串ASCII数字，需要解码转为字符得到flag。
## 操作步骤
1. 打开题目页面，页面不断弹出alert弹窗。
2. 浏览器禁用JavaScript，刷新页面，弹窗停止。
3. 使用`Ctrl+U`查看网页源代码，滚动到源码最底部。
4. 在`<!-- -->`注释中获取一串ASCII数字：
`102 108 97 103 123 52 98 100 101 48 102 102 49 50 101 97 50 52 55 98 99 51 54 102 56 57 98 49 50 99 99 54 56 49 53 51 101 125`
5. 使用ASCII转字符，将数字序列解码，得到flag。
## 知识点总结
1. JavaScript alert弹窗可以干扰页面操作，禁用JS即可绕过弹窗。
2. HTML注释内的内容不会直接展示在网页上，可以用来隐藏信息。
3. ASCII码：数字代表字符，使用`chr()`（Python）或`String.fromCharCode()`（JS）可以将ASCII数字转为文字。
