---
layout: post
title: "Bugku入门逆向 baby.exe"
date: 2026-09-13
categories: CTF
---
# Bugku CTF Writeup｜入门逆向
## 题目信息
- 平台：Bugku
- 类别：Reverse 逆向
- 题目名称：入门逆向
- 附件：file.zip，解压得到 baby.exe

## 题目描述
分析baby.exe程序，找到隐藏flag。

## 解题思路
baby.exe是Windows可执行程序，直接记事本打开会显示二进制乱码，无法阅读。
两种方式可以解题：
1. 使用IDA Pro加载程序，定位main函数，观察汇编中硬编码的十六进制ASCII字符，转换拼接得到flag。
2. 使用在线PE工具，直接读取程序内的字符串，快速提取flag。

## Flag
flag{Re_1s_S0_C0OL}

## 知识点总结
1. exe是二进制文件，记事本打开看到乱码属于正常现象。
2. 简单逆向题经常直接把flag写死在程序的字符串区域，不需要复杂调试。
