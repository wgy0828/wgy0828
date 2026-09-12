---
layout: post
title: "Bugku CTF 计算器 Writeup"
date: 2026-09-12
categories: CTF
tags: [Bugku, WEB, maxlength,前端JS]
---
# 题目：计算器
## 题目描述
页面出现加法计算题，输入框只能输入1个数字，无法直接输入三位数答案。网页JS存在反调试，F12可能打不开。
## 解题思路
考点：input标签maxlength前端输入长度限制。
方法1：查看网页源码，找到code.js，直接读取flag。
方法2：打开开发者工具，修改`maxlength="1"`，解除字符限制，填入算术结果提交。
62+46=108
## 操作步骤
1. 打开题目页面，看到计算题。
2. 使用`Ctrl+U`查看网页源代码。
3. 在源码中找到`code.js`的链接，点击访问，JS源码中直接存在flag。
>备选：`Ctrl+Shift+I`打开开发者工具，定位输入框，将maxlength="1"改为更大数字，输入108，点验证。
## Flag
flag{29f018a4ff479aeaefdaf498bd991e55}
## 知识点总结
1. `maxlength`是前端限制，用户可以直接修改绕过，前端校验不安全。
2. 网页JS文件内可能直接存放flag，查看源码是WEB CTF基础手段。
3. 网页可以写JS拦截F12快捷键，可通过菜单打开开发者工具或者Ctrl+U看源码绕过。
