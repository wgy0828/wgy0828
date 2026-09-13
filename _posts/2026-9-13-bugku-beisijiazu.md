---
layout: post
title: "Bugku Crypto 贝斯家族"
date: 2026-09-13
categories: CTF
---

## 题目信息
- 平台：Bugku CTF
- 类别：Crypto
- 题目名称：贝斯家族
- 作者：harry

## 题目描述
密文：@iH<,{bdR2H;i6*Tm,Wx2izpx2!
“贝斯”是base谐音，属于base家族编码。

## 解题思路
1. 题目名字提示贝斯（base），尝试base系列编码。
2. 密文中包含 @ < , { ! 等特殊符号，base64/32无法包含这类字符，优先尝试base91。
3. 使用在线Base91解码器，输入密文直接解码得到flag。

## Flag
flag{554a5058c9021c76}

## 知识点总结
Base91编码字符集包含大量特殊符号，遇到带有 `@ { < , !` 的base类密文优先考虑base91。
